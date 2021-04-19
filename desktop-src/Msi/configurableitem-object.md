---
description: L'oggetto ConfigurableItem rappresenta una singola riga della tabella ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Oggetto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332625"
---
# <a name="configurableitem-object"></a>Oggetto ConfigurableItem

L' **oggetto ConfigurableItem** rappresenta una singola riga della [tabella ModuleConfiguration](moduleconfiguration-table.md). Si tratta di un singolo "attributo" configurabile del modulo. L'interfaccia è costituita da proprietà di sola lettura, una per ogni colonna nella tabella ModuleConfiguration. La definizione dell'interfaccia è la seguente.

## <a name="members"></a>Membri

L'oggetto **ConfigurableItem** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ConfigurableItem** dispone di queste proprietà.



| Proprietà                                                         | Descrizione                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attributi**](configurableitem-attributes.md)<br/>     | Restituisce il valore nel campo attributi del record di questo oggetto nella tabella ModuleConfiguration.<br/>                            |
| [**Context**](configurableitem-context.md)<br/>           | Restituisce il valore nel campo di contesto del record di questo oggetto nella tabella ModuleConfiguration.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Restituisce il valore nel campo DefaultValue del record di questo oggetto nella tabella ModuleConfiguration.<br/>                          |
| [**Descrizione**](configurableitem-description.md)<br/>   | Restituisce il valore nel campo Descrizione del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | Restituisce il valore nel campo DisplayName del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**Formato**](configurableitem-format.md)<br/>             | Restituisce il valore nel campo formato del record di questo oggetto nella tabella ModuleConfiguration.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Restituisce il valore nel campo HelpKeyword del record di questo oggetto nella tabella ModuleConfiguration.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Restituisce il valore nel campo HelpLocation del record di questo oggetto nella tabella ModuleConfiguration.<br/>                          |
| [**Nome**](configurableitem-name.md)<br/>                 | Restituisce il valore nel campo nome del record di questo oggetto nella [tabella ModuleConfiguration](moduleconfiguration-table.md).<br/> |
| [**Tipo**](configurableitem-type.md)<br/>                 | Restituisce il valore nel campo tipo del record di questo oggetto nella tabella ModuleConfiguration.<br/>                                  |



 

## <a name="c"></a>C++

interfaccia **IMsmConfigurableItem: IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante                      | Valore                                  |
|-------------------------------|----------------------------------------|
| **\_IMSMCONFIGURABLEITEM IID** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




