---
title: XTYP_ADVDATA transazione (Ddeml.h)
description: Informa il client che il valore dell'elemento di dati è stato modificato. La Dynamic Data Exchange callback del client DDE (Dynamic Data Exchange), DdeCallback, riceve questa transazione dopo aver stabilito un ciclo di consulenza con un server.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA dati della transazione Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bf3f3b94f4454547d987ab6536929d1fe2998e7dc0394564143536f1da28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544866"
---
# <a name="xtyp_advdata-transaction"></a>Transazione \_ ADVDATA XTYP

Informa il client che il valore dell'elemento di dati è stato modificato. La Dynamic Data Exchange di callback del client DDE [*,DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve questa transazione dopo aver stabilito un ciclo di consulenza con un server.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Atom di formato dei dati inviati dal server.

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

Handle per i dati associati alla coppia nome argomento e nome dell'elemento. Questo parametro è **NULL** se il client ha specificato il flag **\_ XTYPF NODATA** quando ha richiesto il ciclo di consulenza.

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

Una funzione di callback DDE deve restituire **DDE \_ FACK** se elabora questa **transazione, DDE \_ FBUSY** se è troppo occupato per elaborare la transazione o **DDE \_ FNOTPROCESSED** se rifiuta questa transazione.

## <a name="remarks"></a>Commenti

Un'applicazione non deve liberare l'handle di dati ottenuto durante questa transazione. Un'applicazione deve tuttavia copiare i dati associati all'handle di dati se l'applicazione deve elaborare i dati dopo il completamento della funzione di callback. Un'applicazione può usare [**la funzione DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) per copiare i dati.

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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

