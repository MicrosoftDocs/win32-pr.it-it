---
title: Transazione XTYP_XACT_COMPLETE (DDEML. h)
description: Una funzione di callback client di Dynamic Data Exchange (DDE), DdeCallback, riceve \_ la \_ transazione XTYP XACT complete quando una transazione asincrona, avviata da una chiamata alla funzione DdeClientTransaction, è stata completata.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Scambio di dati delle transazioni XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301280"
---
# <a name="xtyp_xact_complete-transaction"></a>\_ \_ Transazione completa XTYP XACT

Una funzione di callback client di Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione **XTYP \_ XACT \_ complete** quando una transazione asincrona, avviata da una chiamata alla funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , è stata completata.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Il formato dei dati associati alla transazione completata (se applicabile) o **null** se non è stato scambiato alcun dato durante la transazione.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento necessario per la transazione completata.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome dell'elemento richiesto nella transazione completata.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle per i dati necessari nella transazione completata, se applicabile. Se la transazione ha avuto esito positivo, ma non sono presenti dati, questo parametro è **true**. Questo parametro è **null** se la transazione ha avuto esito negativo.

</dd> <dt>

*dwData1* 
</dt> <dd>

Identificatore della transazione completata.

</dd> <dt>

*dwData2* 
</dt> <dd>

Eventuali flag di stato **DDE \_** applicabili nella parola bassa. Questo parametro fornisce supporto per le applicazioni che dipendono da bit **\_ APPSTATUS DDE** . Si consiglia di non usare più questi bit per le applicazioni che potrebbero non essere supportate nelle versioni future del DDEML.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione non deve liberare l'handle di dati ottenuto durante la transazione. Un'applicazione, tuttavia, deve copiare i dati associati all'handle di dati se l'applicazione deve elaborare i dati dopo la restituzione della funzione di callback. Un'applicazione può usare la funzione [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

