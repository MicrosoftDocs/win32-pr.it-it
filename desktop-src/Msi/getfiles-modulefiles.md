---
description: La proprietà ModuleFiles dell'oggetto GetFiles restituisce tutte le chiavi primarie della tabella file per il modulo attualmente aperto.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Proprietà GetFiles. ModuleFiles (Mergemod. h)
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
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332853"
---
# <a name="getfilesmodulefiles-property"></a>Proprietà GetFiles. ModuleFiles

La proprietà **ModuleFiles** dell'oggetto [**GetFiles**](getfiles-object.md) restituisce tutte le chiavi primarie della [tabella file](file-table.md) per il modulo attualmente aperto. Le chiavi primarie vengono restituite come raccolta di stringhe. Il modulo deve essere aperto da una chiamata al metodo [**ApriModulo**](merge-openmodule.md) dell' [oggetto merge](merge-object.md) prima di chiamare **ModuleFiles**.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Si noti che l'ordine dei file elencati nella raccolta potrebbe non trovarsi nella stessa sequenza indicata nella tabella file.

Se il modulo non dispone di una tabella di file o non contiene file nel linguaggio specifico, ModuleFiles restituisce una raccolta di stringhe vuota.

### <a name="c"></a>C++

Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) la funzione ModuleFiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
