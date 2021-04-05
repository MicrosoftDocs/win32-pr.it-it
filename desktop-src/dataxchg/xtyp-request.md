---
title: Transazione XTYP_REQUEST (DDEML. h)
description: Un client utilizza la \_ transazione di richiesta XTYP per richiedere dati da un server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica \_ la richiesta XTYP nella funzione DdeClientTransaction.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- Scambio di dati delle transazioni XTYP_REQUEST
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740327"
---
# <a name="xtyp_request-transaction"></a>\_Transazione di richiesta XTYP

Un client utilizza la transazione di **\_ richiesta XTYP** per richiedere dati da un server. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica la **\_ richiesta XTYP** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato in cui il server deve inviare i dati al client.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome dell'elemento.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il server deve chiamare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per creare un handle di dati che identifichi i dati e quindi restituire l'handle. Il server deve restituire **null** se non è in grado di completare la transazione. Se il server restituisce **null**, il client riceverà un \_ flag FNOTPROCESSED DDE.

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_** requests nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Se la risposta a questa transazione richiede una lunga elaborazione, il server può restituire il \_ codice del blocco CBR per sospendere le transazioni future sulla conversazione corrente, quindi elaborare la transazione in modo asincrono. Al termine del server e se i dati sono pronti per il passaggio al client, il server può chiamare la funzione [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) per riprendere la conversazione.

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

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

