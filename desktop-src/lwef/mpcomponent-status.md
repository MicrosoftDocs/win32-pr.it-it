---
title: Struttura MPCOMPONENT_STATUS (MpClient. h)
description: Informazioni sullo stato del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- Struttura MPCOMPONENT_STATUS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCOMPONENT_STATUS
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
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741023"
---
# <a name="mpcomponent_status-structure"></a>\_Struttura di stato MPCOMPONENT

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

Tipo: **bool**

</dd> <dd>

Stato del componente.

</dd> <dt>

**hResult**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di esito positivo o negativo associato allo stato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





