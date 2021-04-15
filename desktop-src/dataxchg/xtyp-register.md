---
title: Transazione XTYP_REGISTER (DDEML. h)
description: Una funzione di callback Dynamic Data Exchange (DDE), DdeCallback, riceve il \_ tipo di transazione Register XTYP ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione DdeNameService per registrare un nome di servizio o ogni volta che viene avviata un'applicazione non DDEML che supporta l'argomento di sistema.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- Scambio di dati delle transazioni XTYP_REGISTER
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476180"
---
# <a name="xtyp_register-transaction"></a>XTYP \_ registra transazione

Una funzione di callback Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve il tipo di transazione **\_ Register XTYP** ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare un nome di servizio o ogni volta che viene avviata un'applicazione non DDEML che supporta l'argomento di sistema.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Handle per il nome del servizio di base registrato.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome del servizio specifico dell'istanza in fase di registrazione.

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

Un'applicazione non può bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.

Un'applicazione deve utilizzare il parametro *hsz1* per aggiungere il nome del servizio all'elenco di server disponibili per l'utente. Un'applicazione deve utilizzare il parametro *hsz2* per identificare l'istanza dell'applicazione avviata.

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

 

