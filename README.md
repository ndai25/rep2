


select 
case when patindex('%:20:%',[message]) = 0 then '' else  substring (message, patindex('%:20:%',[message])+len('%:20:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:20:%',[message]), 100))-len('%:20:%') ) end as [Transaction Reference Number],
case when patindex('%:23B:%',[message]) = 0 then '' else  substring (message, patindex('%:23B:%',[message])+len('%:23B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:23B:%',[message]), 100))-len('%:23B:%') ) end as [Bank Operation Code],
case when patindex('%:32A:%',[message]) = 0 then '' else  substring (message, patindex('%:32A:%',[message])+len('%:32A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:32A:%',[message]), 100))-len('%:32A:%') ) end as [Value Date / Currency / Interbank Settled],
case when patindex('%:33B:%',[message]) = 0 then '' else  substring (message, patindex('%:33B:%',[message])+len('%:33B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:33B:%',[message]), 100))-len('%:33B:%') ) end as [Currency / Original Ordered Amount],
case when patindex('%:50A:%',[message]) = 0 then '' else  substring (message, patindex('%:50A:%',[message])+len('%:50A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:50A:%',[message]), 100))-len('%:50A:%') ) end as [Ordering Customer (Payer) or Address of the remitter A],
case when patindex('%:50F:%',[message]) = 0 then '' else  substring (message, patindex('%:50F:%',[message])+len('%:50F:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:50F:%',[message]), 100))-len('%:50F:%') ) end as [Ordering Customer (Payer) or Address of the remitter F],
case when patindex('%:50K:%',[message]) = 0 then '' else  substring (message, patindex('%:50K:%',[message])+len('%:50K:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:50K:%',[message]), 100))-len('%:50K:%') ) end as [Ordering Customer (Payer) or Address of the remitter K],
case when patindex('%:52A:%',[message]) = 0 then '' else  substring (message, patindex('%:52A:%',[message])+len('%:52A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:52A:%',[message]), 100))-len('%:52A:%') ) end as [Ordering Institution (Payer's Bank) A],
case when patindex('%:52D:%',[message]) = 0 then '' else  substring (message, patindex('%:52D:%',[message])+len('%:52D:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:52D:%',[message]), 100))-len('%:52D:%') ) end as [Ordering Institution (Payer's Bank) D],
case when patindex('%:53A:%',[message]) = 0 then '' else  substring (message, patindex('%:53A:%',[message])+len('%:53A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:53A:%',[message]), 100))-len('%:53A:%') ) end as [Sender's Correspondent (Bank) A],
case when patindex('%:53B:%',[message]) = 0 then '' else  substring (message, patindex('%:53B:%',[message])+len('%:53B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:53B:%',[message]), 100))-len('%:53B:%') ) end as [Sender's Correspondent (Bank) B],
case when patindex('%:53D:%',[message]) = 0 then '' else  substring (message, patindex('%:53D:%',[message])+len('%:53D:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:53D:%',[message]), 100))-len('%:53D:%') ) end as [Sender's Correspondent (Bank) D],
case when patindex('%:54A:%',[message]) = 0 then '' else  substring (message, patindex('%:54A:%',[message])+len('%:54A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:54A:%',[message]), 100))-len('%:54A:%') ) end as [Receiver's Correspondent (Bank) A],
case when patindex('%:54B:%',[message]) = 0 then '' else  substring (message, patindex('%:54B:%',[message])+len('%:54B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:54B:%',[message]), 100))-len('%:54B:%') ) end as [Receiver's Correspondent (Bank) B],
case when patindex('%:54D:%',[message]) = 0 then '' else  substring (message, patindex('%:54D:%',[message])+len('%:54D:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:54D:%',[message]), 100))-len('%:54D:%') ) end as [Receiver's Correspondent (Bank) D],
case when patindex('%:56A:%',[message]) = 0 then '' else  substring (message, patindex('%:56A:%',[message])+len('%:56A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:56A:%',[message]), 100))-len('%:56A:%') ) end as [Intermediary (Bank) A],
case when patindex('%:56C:%',[message]) = 0 then '' else  substring (message, patindex('%:56C:%',[message])+len('%:56C:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:56C:%',[message]), 100))-len('%:56C:%') ) end as [Intermediary (Bank) C],
case when patindex('%:56D:%',[message]) = 0 then '' else  substring (message, patindex('%:56D:%',[message])+len('%:56D:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:56D:%',[message]), 100))-len('%:56D:%') ) end as [Intermediary (Bank) D],
case when patindex('%:57A:%',[message]) = 0 then '' else  substring (message, patindex('%:57A:%',[message])+len('%:57A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:57A:%',[message]), 100))-len('%:57A:%') ) end as [Account with Institution (Beneficiary's Bank) A],
case when patindex('%:57B:%',[message]) = 0 then '' else  substring (message, patindex('%:57B:%',[message])+len('%:57B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:57B:%',[message]), 100))-len('%:57B:%') ) end as [Account with Institution (Beneficiary's Bank) B],
case when patindex('%:57C:%',[message]) = 0 then '' else  substring (message, patindex('%:57C:%',[message])+len('%:57C:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:57C:%',[message]), 100))-len('%:57C:%') ) end as [Account with Institution (Beneficiary's Bank) C],
case when patindex('%:57D:%',[message]) = 0 then '' else  substring (message, patindex('%:57D:%',[message])+len('%:57D:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:57D:%',[message]), 100))-len('%:57D:%') ) end as [Account with Institution (Beneficiary's Bank) D],
case when patindex('%:59:%',[message]) = 0 then '' else  substring (message, patindex('%:59:%',[message])+len('%:59:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:59:%',[message]), 100))-len('%:59:%') ) end as [Beneficiary],
case when patindex('%:59A:%',[message]) = 0 then '' else  substring (message, patindex('%:59A:%',[message])+len('%:59A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:59A:%',[message]), 100))-len('%:59A:%') ) end as [Beneficiary A],
case when patindex('%:70:%',[message]) = 0 then '' else  substring (message, patindex('%:70:%',[message])+len('%:70:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:70:%',[message]), 100))-len('%:70:%') ) end as [Remittance Information],
case when patindex('%:71A:%',[message]) = 0 then '' else  substring (message, patindex('%:71A:%',[message])+len('%:71A:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:71A:%',[message]), 100))-len('%:71A:%') ) end as [Details of Charges (OUR/SHA/BEN)],
case when patindex('%:72:%',[message]) = 0 then '' else  substring (message, patindex('%:72:%',[message])+len('%:72:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:72:%',[message]), 100))-len('%:72:%') ) end as [Sender to Receiver Information],
case when patindex('%:77B:%',[message]) = 0 then '' else  substring (message, patindex('%:77B:%',[message])+len('%:77B:%'),  patindex('%' + CHAR(10) + '%', substring (message, patindex('%:77B:%',[message]), 100))-len('%:77B:%') ) end as [Regulatory Reporting]
from #s_test
