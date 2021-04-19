---
description: La proprietà TargetPath dell'oggetto Session è una proprietà di lettura/scrittura che fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Proprietà Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333034"
---
# <a name="sessiontargetpath-property"></a>Proprietà Session. TargetPath

La proprietà **targetPath** dell'oggetto [**Session**](session-object.md) è una proprietà di lettura/scrittura che fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Valore proprietà

Obbligatorio nome con distinzione tra maiuscole e minuscole di una proprietà di cartella specificata da una chiave primaria della [tabella di directory](directory-table.md). Se la cartella non esiste, viene generato un errore.

## <a name="remarks"></a>Commenti

Non tentare di configurare il percorso di destinazione se i componenti che utilizzano tali percorsi sono già installati per l'utente corrente o per un altro utente. Controllare la proprietà [**ProductState**](productstate.md) per determinare se il prodotto che contiene il componente è installato.

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




