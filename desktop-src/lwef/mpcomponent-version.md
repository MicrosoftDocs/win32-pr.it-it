---
title: MPCOMPONENT_VERSION (MpClient.h)
description: Versione e ora di aggiornamento per un singolo componente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION funzionalità dell'ambiente Windows legacy
- PMPCOMPONENT_VERSION puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976071"
---
# <a name="mpcomponent_version-structure"></a>Struttura MPCOMPONENT \_ VERSION

Versione e ora di aggiornamento per un singolo componente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Members

<dl> <dt>

**Version**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Campo Versione. Ogni **parola** rappresenta principale, secondaria, build e revisione.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora dell'ultimo aggiornamento del componente, in **formato FILETIME.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





