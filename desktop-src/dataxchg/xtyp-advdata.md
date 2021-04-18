---
title: Transazione XTYP_ADVDATA (DDEML. h)
description: Informa il client che il valore dell'elemento di dati è stato modificato. La funzione di callback del client Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione dopo aver stabilito un ciclo di notifica con un server.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Scambio di dati delle transazioni XTYP_ADVDATA
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
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301093"
---
# <a name="xtyp_advdata-transaction"></a>\_Transazione ADVDATA XTYP

Informa il client che il valore dell'elemento di dati è stato modificato. La funzione di callback del client Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione dopo aver stabilito un ciclo di notifica con un server.


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

Formato Atom dei dati inviati dal server.

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

Handle per i dati associati alla coppia nome argomento e nome elemento. Questo parametro è **null** se il client ha specificato il flag **\_ NoData XTYPF** quando ha richiesto il ciclo di notifica.

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

Una funzione di callback DDE deve **restituire \_ fack DDE** se elabora questa transazione, **\_ FBUSY DDE** se è troppo occupato per elaborare la transazione o **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.

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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

