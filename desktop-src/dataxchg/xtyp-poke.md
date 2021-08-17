---
title: XTYP_POKE transazione (Ddeml.h)
description: Un client usa la transazione POKE XTYP \_ per inviare dati non richiesta al server. Una funzione di callback del server Dynamic Data Exchange (DDE) DdeCallback riceve questa transazione quando un client specifica poKE XTYP nella \_ funzione DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE dati della transazione Exchange
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
ms.openlocfilehash: a179f4130ae06c4548b52586d6086201c2d832a158cef877d9aaf524160f4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914751"
---
# <a name="xtyp_poke-transaction"></a>Transazione \_ POKE XTYP

Un client usa la **\_ transazione POKE XTYP** per inviare dati non richiesta al server. Una funzione di callback del server Dynamic Data Exchange [*(DDE) DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve questa transazione quando un client specifica **\_ poKE XTYP** nella [**funzione DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


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

Formato dei dati inviati dal server.

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

Una funzione di callback del server deve restituire il flag **DDE \_ FACK** se elabora questa transazione, il flag **DDE \_ FBUSY** se è troppo occupato per elaborare la transazione o il flag **DDE \_ FNOTPROCESSED** se rifiuta la transazione.

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **\_ CBF FAIL \_ POKES** nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

