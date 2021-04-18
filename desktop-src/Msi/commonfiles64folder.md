---
description: Il programma di installazione imposta la proprietà CommonFiles64Folder sul percorso completo della cartella dei file comuni a 64 bit predefinita. La proprietà CommonFilesFolder esistente è impostata sulla cartella a 32 bit corrispondente.
ms.assetid: 6730170a-0f73-4a84-b3fb-bd15c72917c7
title: Proprietà CommonFiles64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44a6720e609cfa79cd0e4adbfd5136c7a92a5ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328779"
---
# <a name="commonfiles64folder-property"></a>Proprietà CommonFiles64Folder

Il programma di installazione imposta la proprietà **CommonFiles64Folder** sul percorso completo della cartella dei file comuni a 64 bit predefinita. La proprietà [**CommonFilesFolder**](commonfilesfolder.md) esistente è impostata sulla cartella a 32 bit corrispondente.

## <a name="remarks"></a>Commenti

Il programma di installazione imposta questa proprietà su Windows a 64 bit. Questa proprietà non viene utilizzata in Windows a 32 bit. Quando si usa Windows a 64 bit, il valore può essere "C: \\ Programmi file \\ comuni".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




