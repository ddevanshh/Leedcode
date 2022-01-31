# Leedcode


class Solution {
public:
    string longestCommonPrefix(vector<string>& strs) {
        int mi=INT_MAX;
        for(int i=0;i<strs.size();i++){
            if(strs[i].size()<mi){
                mi=strs[i].size();
            }
            
        }
        string s="";
        for(int i=0;i<mi;i++){
            s+=strs[0][i];
            for(int j=0;j<strs.size();j++){
                if(strs[j][i]!=s[i]){
                    s.pop_back();
                    return s;
                }
            
                
            }
        }
        return s;
        
    }
};
