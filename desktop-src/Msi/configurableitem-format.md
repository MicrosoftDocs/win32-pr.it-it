---
description: La proprietà Format dell'oggetto ConfigurableItem restituisce il valore della colonna Format della tabella ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Proprietà ConfigurableItem. Format (Mergemod. h)
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
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328071"
---
# <a name="configurableitemformat-property"></a>Proprietà ConfigurableItem. Format

La proprietà **Format** dell'oggetto [**ConfigurableItem**](configurableitem-object.md) restituisce il valore della colonna Format della [tabella ModuleConfiguration](moduleconfiguration-table.md).

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

Vedere [**ottenere \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) la funzione Format.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




