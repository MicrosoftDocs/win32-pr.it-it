---
description: La proprietà manifest viene utilizzata per impostare o ottenere il contesto di attivazione attiva.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Proprietà ActCtx. manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966601"
---
# <a name="actctxmanifest-property"></a>Proprietà ActCtx. manifest

La proprietà **manifest** viene utilizzata per impostare o ottenere il contesto di attivazione attiva.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se è possibile creare un contesto di attivazione con il file manifesto specificato, lo script seguente imposta la proprietà del manifesto e attiva la costante di attivazione specificata dal manifesto. Se non è possibile creare un contesto di attivazione dal manifesto, il contesto di attivazione rimane impostato sul contesto di attivazione attualmente attivo.

ActCtxObj. manifest = "<*nome file manifesto*>";

Se un contesto di attivazione è stato creato o attivato in precedenza, lo script seguente imposta la proprietà **manifest** sul contesto di attivazione corrente. Se un contesto di attivazione non è stato creato o attivato in precedenza, imposta la proprietà del **manifesto** su una stringa vuota.

"BSTR bstrManifest = ActCtxObj. manifest"

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx è definito come 8FA7728F-B69B-4ee5-99F2-E2AA021BEF28<br/>           |



 

 




