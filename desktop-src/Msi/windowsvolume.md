---
description: Il programma di installazione imposta la proprietà WindowsVolume sul volume della cartella windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Proprietà WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3e0632fa981e9ea511be5017d02411bb6bb18355187c818ac3cd6c39e4f670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989935"
---
# <a name="windowsvolume-property"></a>Proprietà WindowsVolume

Il programma di installazione imposta **la proprietà WindowsVolume** sul volume della cartella windows. La proprietà termina sempre con una barra rovesciata. Può essere usato per impostare il percorso predefinito sul volume in cui si trova la cartella Windows perché la [**proprietà ROOTDRIVE**](rootdrive.md) non è necessariamente uguale a questa unità.

## <a name="remarks"></a>Commenti

Non usare la **proprietà WindowsVolume** nella colonna Directory della [tabella](directory-table.md) Directory. La [**proprietà WindowsFolder**](windowsfolder.md) contiene il percorso della Windows cartella.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione in Windows Server 2003 o Windows XP Vedere Windows Installer Run-Time Requirements (Requisiti del Run-Time del programma di installazione [di Windows)](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione del programma di Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




