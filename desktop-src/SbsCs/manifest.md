---
description: La proprietà Manifesto viene usata per impostare o ottenere il contesto di attivazione attivo.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx.Manifest - proprietà
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
ms.openlocfilehash: 77d45bd0dc97ed99ee976da4e262ed3d4819b0ec4c744a4e0a8d76b98f5bacd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977231"
---
# <a name="actctxmanifest-property"></a>ActCtx.Manifest - proprietà

La **proprietà Manifesto** viene usata per impostare o ottenere il contesto di attivazione attivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se è possibile creare un contesto di attivazione con il file manifesto fornito, lo script seguente imposta la proprietà Manifesto e attiva la costante di attivazione specificata dal manifesto. Se non è possibile creare un contesto di attivazione dal manifesto, il contesto di attivazione rimane impostato sul contesto di attivazione attualmente attivo.

ActCtxObj.Manifest = "<*nome file manifesto*>";

Se in precedenza è stato creato o attivato un contesto di attivazione, lo script seguente imposta la **proprietà Manifesto** sul contesto di attivazione corrente. Se in precedenza non è stato creato o attivato un contesto di attivazione, la **proprietà Manifesto** viene impostata su una stringa vuota.

"BSTR bstrManifest = ActCtxObj.Manifest"

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID IActCtx è definito come \_ 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




