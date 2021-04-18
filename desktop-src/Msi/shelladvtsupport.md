---
description: La proprietà ShellAdvtSupport viene impostata dal programma di installazione se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Proprietà ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324410"
---
# <a name="shelladvtsupport-property"></a>Proprietà ShellAdvtSupport

La proprietà **ShellAdvtSupport** viene impostata dal programma di installazione se l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione.

## <a name="remarks"></a>Commenti

Se questa proprietà è impostata, l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione. Questa operazione è supportata da Windows 2000 e dai sistemi che eseguono Internet Explorer 4,01. Se questa proprietà non è impostata, il programma di installazione ha il comportamento predefinito della creazione di funzionalità non annunciate durante l'installazione, localmente o in esecuzione dall'origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Supporto della piattaforma per gli annunci](platform-support-of-advertisement.md)
</dt> </dl>

 

 
