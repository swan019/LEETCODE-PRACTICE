# LEETCODE-PRACTICE

    vector<int> intersection(vector<int>& nums1, vector<int>& nums2) {
        vector<int> fv;
        vector<int> sv;
        unordered_map<int, int> fp;
        unordered_map<int, int> sp;
        unordered_map<int, int> rp;
        vector<int> rv;
        vector<int> ans;

        for(int i = 0; i < nums1.size(); ++i)
        {
            fp[nums1[i]]++;
        }

        for(auto it : fp)
        {
            fv.push_back(it.first);
        }

        for(int i = 0; i < nums2.size(); ++i)
        {
            sp[nums2[i]]++;
        }

        for(auto itt : sp)
        {
            sv.push_back(itt.first);
        }

        for(int i = 0; i < fv.size(); ++i)
        {
            rv.push_back(fv[i]);
        }

        for(int i = 0; i < sv.size(); ++i)
        {
            rv.push_back(sv[i]);
        }

        for(int i = 0; i < rv.size(); ++i)
        {
            rp[rv[i]]++;
        }

        for(auto itr : rp)
        {
            if(itr.second >= 2)
            {
                ans.push_back(itr.first);
            }
        }

        return ans;

    }
