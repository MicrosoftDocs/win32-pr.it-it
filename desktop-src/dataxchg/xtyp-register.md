---
title: XTYP_REGISTER transazione (Ddeml.h)
description: Una funzione di callback di Dynamic Data Exchange (DDE), DdeCallback, riceve il tipo di transazione XTYP REGISTER ogni volta che un'applicazione \_ server Dynamic Data Exchange Management Library (DDEML) usa la funzione DdeNameService per registrare un nome di servizio o ogni volta che viene avviata un'applicazione non DDEML che supporta l'argomento System.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER dati transazione Exchange
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
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544750"
---
# <a name="xtyp_register-transaction"></a>Transazione REGISTER \_ XTYP

Una funzione di callback DDE (Dynamic Data Exchange), [*DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve il tipo di transazione **XTYP \_ REGISTER** ogni volta che un'applicazione server DDEML (Dynamic Data Exchange Management Library) usa la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare un nome di servizio o ogni volta che viene avviata un'applicazione non DDEML che supporta l'argomento System.


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

Handle per il nome del servizio specifico dell'istanza registrato.

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

Questa transazione viene filtrata se l'applicazione ha specificato il flag **CBF \_ SKIP \_ REGISTRATIONS** nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un'applicazione non può bloccare questo tipo di transazione. Il **codice restituito CBR \_ BLOCK** viene ignorato.

Un'applicazione deve usare il *parametro hsz1* per aggiungere il nome del servizio all'elenco di server disponibili per l'utente. Un'applicazione deve usare il *parametro hsz2* per identificare l'istanza dell'applicazione avviata.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

