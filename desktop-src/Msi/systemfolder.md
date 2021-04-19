---
description: Il programma di installazione imposta la proprietà SystemFolder sul percorso completo della cartella di sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Proprietà SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330144"
---
# <a name="systemfolder-property"></a>Proprietà SystemFolder

Il programma di installazione imposta la proprietà **SystemFolder** sul percorso completo della cartella di sistema.

## <a name="remarks"></a>Commenti

Questa proprietà viene impostata dal programma di installazione. Ad esempio, in Windows a 32 bit il valore può essere C: \\ Windows \\ system32. In Windows a 64 bit il valore può essere C: \\ Windows \\ SysWow64.

Questa cartella è in genere una sottodirectory della cartella Windows. Tuttavia, si trova in un server se configurato per le finestre condivise.

Questa cartella è locale, anche se configurata per le finestre condivise.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




