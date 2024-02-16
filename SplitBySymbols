std::vector<std::string> SplitAddress(const std::string& _str)
{
	auto is_delimeter = [](char c) { return c == ',' || c == ';'; };
	std::vector<std::string> result;
	auto pos = std::find_if(_str.begin(), _str.end(), is_delimeter);
	auto cur_beg = _str.begin();

	while (pos != _str.end())
	{
		result.push_back(std::string(cur_beg, pos));
		cur_beg = next(pos, 1);
		pos = std::find_if(cur_beg, _str.end(), is_delimeter);
	}

	result.push_back(std::string(cur_beg, _str.end()));
	return result;
}
