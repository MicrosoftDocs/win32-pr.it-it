---
title: Struttura MPSCAN_RESOURCES (MpClient. h)
description: Informazioni sulle risorse passate durante un'operazione di analisi.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Struttura MPSCAN_RESOURCES le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_RESOURCES
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
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964947"
---
# <a name="mpscan_resources-structure"></a>\_Struttura delle risorse di MPSCAN

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

**origine dati**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Matrice di risorse. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni MPRESOURCE**](mpresource-info.md)
</dt> </dl>

 

 





