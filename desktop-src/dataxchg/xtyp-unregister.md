---
title: Transazione XTYP_UNREGISTER (DDEML. h)
description: Una funzione di callback Dynamic Data Exchange (DDE), DdeCallback, riceve la \_ transazione di annullamento della registrazione di XTYP ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione DdeNameService per annullare la registrazione di un nome di servizio o ogni volta che un'applicazione non DDEML che supporta l'argomento di sistema viene terminata.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Scambio di dati delle transazioni XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742871"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ Annulla registrazione transazione

Una funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve la transazione di **annullamento della \_ registrazione di XTYP** ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per annullare la registrazione di un nome di servizio o ogni volta che un'applicazione non DDEML che supporta l'argomento di sistema viene terminata.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle per il nome del servizio di base di cui viene annullata la registrazione.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome del servizio specifico dell'istanza di cui viene annullata la registrazione.

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

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione ha specificato il flag **CBF \_ Skip \_ registrations** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un'applicazione non può bloccare questo tipo di transazione. il \_ codice restituito del blocco CBR viene ignorato.

Un'applicazione deve utilizzare il parametro *hsz1* per rimuovere il nome del servizio dall'elenco dei server disponibili per l'utente. Un'applicazione deve utilizzare il parametro *hsz2* per identificare l'istanza dell'applicazione terminata.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

