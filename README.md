# 24bda70111-cc-groupA-gagan-singh-exp2.2.2

class Solution {
public:
    TreeNode* inorderSuccessor(TreeNode* root, TreeNode* p) {
        TreeNode* ans = nullptr;

        while (root != nullptr) {
            if (root->val > p->val) {
                // root is a possible successor
                ans = root;

                // Try to find a smaller successor
                root = root->left;
            }
            else {
                // root is <= p, so successor must be on the right
                root = root->right;
            }
        }

        return ans;
    }
};
