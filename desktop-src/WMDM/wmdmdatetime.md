---
title: Struttura WMDMDATETIME
description: La struttura WMDMDATETIME contiene una data e un'ora del giorno.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Struttura WMDMDATETIME Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMDATETIME Windows Media Gestione dispositivi
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
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324403"
---
# <a name="wmdmdatetime-structure"></a>Struttura WMDMDATETIME

La struttura **WMDMDATETIME** contiene una data e un'ora del giorno.

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

Parola contenente il secondo (0-59).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMDSPStorage:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[**IWMDMStorage:: GETDATE**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[**WMDMRIGHTS**](wmdmrights.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





