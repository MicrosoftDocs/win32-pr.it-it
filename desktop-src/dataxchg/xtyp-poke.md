---
title: Transazione XTYP_POKE (DDEML. h)
description: Un client utilizza la \_ transazione poke XTYP per inviare dati non richiesti al server. Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve questa transazione quando un client specifica XTYP \_ poke nella funzione DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Scambio di dati delle transazioni XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964131"
---
# <a name="xtyp_poke-transaction"></a>\_Transazione poke XTYP

Un client utilizza la **transazione \_ poke XTYP** per inviare dati non richiesti al server. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ poke** nella funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Il formato dei dati inviati dal server.

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

Handle per i dati inviati dal client al server.

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

Una funzione di callback del server deve restituire il flag **\_ fack DDE** se elabora questa transazione, il flag **\_ FBUSY DDE** se è troppo occupato per elaborare la transazione o il flag **\_ FNOTPROCESSED DDE** se rifiuta questa transazione.

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ pokes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

