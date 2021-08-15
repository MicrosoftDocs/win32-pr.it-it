---
title: MPSCAN_RESOURCES struttura (MpClient.h)
description: Informazioni sulle risorse passate durante un'operazione di analisi.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES struttura Legacy Windows Environment Features
- PMPSCAN_RESOURCES puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747350"
---
# <a name="mpscan_resources-structure"></a>Struttura MPSCAN \_ RESOURCES

Informazioni sulle risorse passate durante un'operazione di analisi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Members

<dl> <dt>

**dwResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di risorse.

</dd> <dt>

**pResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Matrice di risorse. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SU \_ MPRESOURCE**](mpresource-info.md)
</dt> </dl>

 

 





