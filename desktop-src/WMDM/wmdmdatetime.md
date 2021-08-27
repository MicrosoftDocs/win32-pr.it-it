---
title: Struttura WMDMDATETIME
description: La struttura WMDMDATETIME contiene una data e un'ora del giorno.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Struttura WMDMDATETIME windows Media Device Manager
- Puntatore alla struttura PWMDMDATETIME windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9648b4c2d1272dcf00d45277119b51f438dba23d9eaf5e7810451fb693e8cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004631"
---
# <a name="wmdmdatetime-structure"></a>Struttura WMDMDATETIME

La **struttura WMDMDATETIME** contiene una data e un'ora del giorno.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a>Members

<dl> <dt>

**wYear**
</dt> <dd>

Parola contenente l'anno a quattro cifre.

</dd> <dt>

**wMonth**
</dt> <dd>

Parola contenente il mese (1-12).

</dd> <dt>

**wDay**
</dt> <dd>

Parola contenente il giorno del mese (1-31).

</dd> <dt>

**wHour**
</dt> <dd>

Parola contenente l'ora (0-23).

</dd> <dt>

**wMinute**
</dt> <dd>

Parola contenente il minuto (0-59).

</dd> <dt>

**wSecond**
</dt> <dd>

Parola contenente la seconda (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage::GetDate**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





