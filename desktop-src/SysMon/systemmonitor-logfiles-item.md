---
title: Proprietà LogFiles. Item
description: Recupera l'istanza di LogFileItem specificata dalla raccolta.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Proprietà Item SysMon
- Proprietà Item SysMon, classe LogFiles
- Classe LogFiles SysMon, proprietà Item
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048096"
---
# <a name="logfilesitem-property"></a>Proprietà LogFiles. Item

Recupera l'istanza di [**LogFileItem**](logfileitem.md) specificata dalla raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valore proprietà

Istanza di [**LogFileItem**](logfileitem.md) che corrisponde al valore di indice specificato.

## <a name="remarks"></a>Commenti

Si tratta della proprietà predefinita dell'oggetto [**LogFiles**](systemmonitor-logfiles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





