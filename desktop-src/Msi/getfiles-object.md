---
description: L'oggetto GetFiles recupera i file necessari in una determinata lingua del modulo. Richiede che alcune azioni vengano eseguite tramite l'oggetto merge prima che tutte le parti di questa interfaccia restituiscono risultati validi.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Oggetto GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332848"
---
# <a name="getfiles-object"></a>GetFiles (oggetto)

L'oggetto **GetFiles** recupera i file necessari in una determinata lingua del modulo. Richiede che alcune azioni vengano eseguite tramite l' [oggetto merge](merge-object.md) prima che tutte le parti di questa interfaccia restituiscono risultati validi.

## <a name="members"></a>Membri

L'oggetto **GetFiles** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **GetFiles** dispone di queste proprietà.



| Proprietà                                               | Descrizione                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ModuleFiles**](getfiles-modulefiles.md)<br/> | La proprietà [**ModuleFiles**](getfiles-modulefiles.md) restituisce tutte le chiavi primarie della [tabella file](file-table.md) per il modulo attualmente aperto.<br/> |



 

## <a name="c"></a>C++

interfaccia **IMsmGetFiles: IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante              | Valore                                  |
|-----------------------|----------------------------------------|
| **\_IMSMGETFILES IID** | {7041AE26-2D78-11D2-888A-00A0C981B015} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




