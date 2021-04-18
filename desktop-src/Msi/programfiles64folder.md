---
description: Il programma di installazione imposta la proprietà ProgramFiles64Folder sul percorso completo della cartella dei file di programma a 64 bit predefiniti. La proprietà ProgramFilesFolder esistente è impostata sulla cartella a 32 bit corrispondente.
ms.assetid: 9301628a-3d56-4d0a-aab5-88663742daa1
title: Proprietà ProgramFiles64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb8b85e0a433a3a4b51cfe23ef2de1f75dba09c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330379"
---
# <a name="programfiles64folder-property"></a>Proprietà ProgramFiles64Folder

Il programma di installazione imposta la proprietà **ProgramFiles64Folder** sul percorso completo della cartella dei file di programma a 64 bit predefiniti. La proprietà [**ProgramFilesFolder**](programfilesfolder.md) esistente è impostata sulla cartella a 32 bit corrispondente.

## <a name="remarks"></a>Commenti

Questa proprietà viene impostata dal programma di installazione. Ad esempio, in Windows a 64 bit, il valore può essere C: \\ Program Files. Questa proprietà non viene utilizzata in Windows a 32 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




