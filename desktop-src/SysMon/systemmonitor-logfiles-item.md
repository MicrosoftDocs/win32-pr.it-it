---
title: LogFiles.Item - proprietà
description: Recupera l'istanza di LogFileItem specificata dalla raccolta.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Proprietà Item SysMon
- Proprietà Item SysMon , classe LogFiles
- Classe LogFiles SysMon , proprietà Item
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
ms.openlocfilehash: b2441575ec45c3d914fef80d5a7c6655b76597c094e319f5f0b01dbb62190e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882282"
---
# <a name="logfilesitem-property"></a>LogFiles.Item - proprietà

Recupera [**l'istanza di LogFileItem**](logfileitem.md) specificata dalla raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a>Valore proprietà

[**Istanza di LogFileItem**](logfileitem.md) che corrisponde al valore di indice specificato.

## <a name="remarks"></a>Commenti

Si tratta della proprietà predefinita [**dell'oggetto LogFiles.**](systemmonitor-logfiles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 





