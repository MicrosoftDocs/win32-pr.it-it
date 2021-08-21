---
description: La proprietà ModuleFiles dell'oggetto GetFiles restituisce tutte le chiavi primarie della tabella File per il modulo attualmente aperto.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Proprietà GetFiles.ModuleFiles (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b4b7d498979c94de048e72058df4c8bf87fb8607220efe808554d66deb5d89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635941"
---
# <a name="getfilesmodulefiles-property"></a>Proprietà GetFiles.ModuleFiles

**La proprietà ModuleFiles** [**dell'oggetto GetFiles**](getfiles-object.md) restituisce tutte le chiavi primarie della tabella [File](file-table.md) per il modulo attualmente aperto. Le chiavi primarie vengono restituite come una raccolta di stringhe. Il modulo deve essere aperto da una chiamata al [**metodo OpenModule**](merge-openmodule.md) dell'oggetto [Merge](merge-object.md) prima di **chiamare ModuleFiles**.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Si noti che l'ordine dei file elencati nella raccolta potrebbe non essere nella stessa sequenza elencata nella tabella File.

Se il modulo non ha una tabella File o non contiene file nel linguaggio specifico, ModuleFiles restituisce una raccolta vuota di stringhe.

### <a name="c"></a>C++

Vedere [**la funzione get \_ ModuleFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
