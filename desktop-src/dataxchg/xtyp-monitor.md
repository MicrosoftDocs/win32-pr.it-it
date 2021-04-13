---
title: Transazione XTYP_MONITOR (DDEML. h)
description: Una funzione di callback DDE del debugger Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di monitoraggio XTYP ogni volta che si verifica un evento DDE nel sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Scambio di dati delle transazioni XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400512"
---
# <a name="xtyp_monitor-transaction"></a>\_Transazione monitoraggio XTYP

Una funzione di callback DDE del debugger Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ monitoraggio XTYP** ogni volta che si verifica un evento DDE nel sistema. Per ricevere questa transazione, un'applicazione deve specificare il valore di **\_ monitoraggio APPCLASS** quando chiama la funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non usato.

</dd> <dt>

*hconv* 
</dt> <dd>

Non usato.

</dd> <dt>

*hsz1* 
</dt> <dd>

Non usato.

</dd> <dt>

*hsz2* 
</dt> <dd>

Non usato.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle per un oggetto DDE che contiene informazioni sull'evento DDE. L'applicazione deve usare la funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) per ottenere un puntatore all'oggetto.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData2* 
</dt> <dd>

Evento DDE. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ CALLBACK**</dt> <dt>0x08000000</dt> </dl> | Il sistema ha inviato una transazione a una funzione di callback DDE. L'oggetto DDE contiene una struttura [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) che fornisce informazioni sulla transazione.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_**</dt> <dt>0x40000000</dt> Conv </dl>                | Una conversazione DDE è stata stabilita o terminata. L'oggetto DDE contiene una struttura [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) che fornisce informazioni sulla conversazione.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ ERRORI**</dt> <dt>0x10000000</dt> </dl>          | Si è verificato un errore DDE. L'oggetto DDE contiene una struttura [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) che fornisce informazioni sull'errore.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt> </dl>   | Un'applicazione DDE ha creato, rilasciato o incrementato il conteggio di utilizzo di un handle di stringa oppure è stato liberato un handle di stringa come risultato di una chiamata alla funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . L'oggetto DDE contiene una struttura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) che fornisce informazioni sull'handle di stringa.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ COLLEGAMENTI**</dt> <dt>0x20000000</dt> </dl>             | Un'applicazione DDE ha avviato o arrestato un ciclo di notifica. L'oggetto DDE contiene una struttura [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) che fornisce informazioni sul ciclo di notifica.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_**</dt> <dt>0x04000000</dt> POSTMSGS </dl>    | Il sistema o un'applicazione ha inviato un messaggio DDE. L'oggetto DDE contiene una struttura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) che fornisce informazioni sul messaggio.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_**</dt> <dt>0x02000000</dt> SENDMSGS </dl>    | Il sistema o un'applicazione ha inviato un messaggio DDE. L'oggetto DDE contiene una struttura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) che fornisce informazioni sul messaggio.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione di callback elabora questa transazione, deve restituire 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>DDEML. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

