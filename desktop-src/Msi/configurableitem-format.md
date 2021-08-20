---
description: La proprietà Format dell'oggetto ConfigurableItem restituisce il valore della colonna Format della tabella ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Proprietà ConfigurableItem.Format (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ee8770029c8465d1e1a60349010847ff38fdac928bb61cd02b0e5a2b034538c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144006"
---
# <a name="configurableitemformat-property"></a>ConfigurableItem.Format - proprietà

La **proprietà Format** [**dell'oggetto ConfigurableItem**](configurableitem-object.md) restituisce il valore della colonna Format della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà può avere solo i valori seguenti.



| Costante                        | Valore |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

Vedere [**la funzione get \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) Format.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




