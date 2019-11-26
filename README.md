# siqi
# time yourself whenever you are processing something in order for future improvements

declare 
cursor cur_all is select * from sx_account;
    v_start_nr number;
    v_end_nr number;
    v_elapsed_nr number;
begin
    v_start_nr:=dbms_utility.get_time();
    #code goes here
    
    
    
    #end of code
    v_end_nr:=dbms_utility.get_time();
    v_elapsed_nr:=v_end_nr-v_start_nr;
    dbms_output.put_line('Elapsed;'||v_elapsed_nr/100||'secs.');
end;
