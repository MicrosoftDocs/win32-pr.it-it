---
title: Transazione XTYP_DISCONNECT (DDEML. h)
description: La funzione di callback Dynamic Data Exchange (DDE) di un'applicazione, DdeCallback, riceve la \_ transazione di disconnessione XTYP quando il partner dell'applicazione in una conversazione usa la funzione DdeDisconnect per terminare la conversazione.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Scambio di dati delle transazioni XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740330"
---
# <a name="xtyp_disconnect-transaction"></a>\_Transazione disconnessione XTYP

La funzione di callback Dynamic Data Exchange (DDE) di un'applicazione, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **\_ disconnessione XTYP** quando il partner dell'applicazione in una conversazione usa la funzione [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) per terminare la conversazione.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle a che la conversazione è stata terminata.

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

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData2* 
</dt> <dd>

Specifica se i partner nella conversazione sono la stessa istanza dell'applicazione. Se questo parametro è 1, i partner sono la stessa istanza. Se questo parametro è 0, i partner sono istanze diverse.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione ha specificato il flag **CBF \_ Skip \_ disconnectes** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

L'applicazione può ottenere lo stato della conversazione terminata chiamando la funzione [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante l'elaborazione della transazione. L'handle di conversazione diventa non valido dopo la restituzione della funzione di callback.

Un'applicazione non può bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.

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

[**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

