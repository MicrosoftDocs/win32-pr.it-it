---
title: MPCOMPONENT_STATUS struttura (MpClient.h)
description: Informazioni sullo stato del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS struttura Legacy Windows Environment Features
- PMPCOMPONENT_STATUS puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747799"
---
# <a name="mpcomponent_status-structure"></a>Struttura MPCOMPONENT \_ STATUS

Informazioni sullo stato del componente.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**fEnable**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

Stato per il componente.

</dd> <dt>

**Hresult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di esito positivo o negativo associato allo stato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





