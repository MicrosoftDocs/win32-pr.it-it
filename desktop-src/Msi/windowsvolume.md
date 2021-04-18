---
description: Il programma di installazione imposta la proprietà WindowsVolume sul volume della cartella Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Proprietà WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328750"
---
# <a name="windowsvolume-property"></a>Proprietà WindowsVolume

Il programma di installazione imposta la proprietà **WindowsVolume** sul volume della cartella Windows. La proprietà termina sempre con una barra rovesciata. Questa operazione può essere utilizzata per impostare il percorso predefinito sul volume in cui si trova la cartella Windows, perché la proprietà [**ROOTDRIVE**](rootdrive.md) non è necessariamente uguale a questa unità.

## <a name="remarks"></a>Commenti

Non utilizzare la proprietà **WindowsVolume** nella colonna directory della tabella [directory](directory-table.md) . La proprietà [**WindowsFolder**](windowsfolder.md) contiene il percorso della cartella Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




