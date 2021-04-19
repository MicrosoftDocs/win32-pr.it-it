---
description: La proprietà SourcePath dell'oggetto Session è una proprietà di sola lettura che fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine server.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Proprietà Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333035"
---
# <a name="sessionsourcepath-property"></a>Proprietà Session. SourcePath

La proprietà **SourcePath** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine server.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Valore proprietà

Obbligatorio nome con distinzione tra maiuscole e minuscole di una proprietà di cartella specificata da una chiave primaria della [tabella di directory](directory-table.md). Se la cartella non esiste, viene generato un errore.

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




