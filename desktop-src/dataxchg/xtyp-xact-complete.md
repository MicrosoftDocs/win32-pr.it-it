---
title: XTYP_XACT_COMPLETE transazione (Ddeml.h)
description: Una funzione di callback client Dynamic Data Exchange (DDE), DdeCallback, riceve la transazione XTYP XACT COMPLETE al completamento di una transazione asincrona, avviata da una chiamata alla funzione \_ \_ DdeClientTransaction.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE transazione dati Exchange
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
ms.openlocfilehash: 2d3833207371bbfab059f67ecb5bdb72b77334ef3ffc73618e013ce137835c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678011"
---
# <a name="xtyp_xact_complete-transaction"></a>Transazione \_ XTYP XACT \_ COMPLETE

Una funzione di callback client Dynamic Data Exchange [*(DDE), DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione **\_ XTYP XACT \_ COMPLETE** al completamento di una transazione asincrona, avviata da una chiamata alla funzione [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


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

Formato dei dati associati alla transazione completata (se applicabile) o **NULL** se non è stato scambiato alcun dato durante la transazione.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento coinvolto nella transazione completata.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome dell'elemento coinvolto nella transazione completata.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle per i dati coinvolti nella transazione completata, se applicabile. Se la transazione ha avuto esito positivo ma non ha coinvolto dati, questo parametro è **TRUE.** Questo parametro è **NULL se** la transazione ha avuto esito negativo.

</dd> <dt>

*dwData1* 
</dt> <dd>

Identificatore della transazione completata.

</dd> <dt>

*dwData2* 
</dt> <dd>

Tutti i flag di stato **DDE \_** applicabili nella parola bassa. Questo parametro fornisce il supporto per le applicazioni dipendenti dai bit **\_ APPSTATUS DDE.** È consigliabile che le applicazioni non usino più questi bit che potrebbero non essere supportati nelle versioni future di DDEML.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione non deve liberare l'handle di dati ottenuto durante questa transazione. Un'applicazione deve tuttavia copiare i dati associati all'handle di dati se l'applicazione deve elaborare i dati dopo la funzione di callback. Un'applicazione può usare [**la funzione DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Ddeml.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

