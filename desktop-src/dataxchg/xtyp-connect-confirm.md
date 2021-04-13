---
title: Transazione XTYP_CONNECT_CONFIRM (DDEML. h)
description: Una funzione di callback del server Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ conferma della transazione XTYP Connect \_ per confermare che è stata stabilita una conversazione con un client e per fornire al server l'handle di conversazione.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Scambio di dati delle transazioni XTYP_CONNECT_CONFIRM
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400684"
---
# <a name="xtyp_connect_confirm-transaction"></a>\_ \_ Conferma transazione connessione XTYP

Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la conferma della transazione **XTYP \_ Connect \_** per confermare che è stata stabilita una conversazione con un client e per fornire al server l'handle di conversazione. Questa transazione viene inviata dal sistema come risultato di una transazione [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) precedente.


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle per la nuova conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento in cui è stata stabilita la conversazione.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome del servizio in cui è stata stabilita la conversazione.

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

Specifica se il client è la stessa istanza dell'applicazione del server. Se il parametro è 1, il client è la stessa istanza. Se il parametro è 0, il client è un'istanza diversa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server specificata **CBF \_ Skip \_ Connect \_ conferma** flag nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un server non è in grado di bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

