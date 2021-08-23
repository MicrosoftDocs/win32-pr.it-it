---
description: La proprietà ShellAdvtSupport viene impostata dal programma di installazione se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: ShellAdvtSupport - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628441"
---
# <a name="shelladvtsupport-property"></a>ShellAdvtSupport - proprietà

La **proprietà ShellAdvtSupport** viene impostata dal programma di installazione se l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione.

## <a name="remarks"></a>Commenti

Se questa proprietà è impostata, l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione. Questa funzionalità è supportata da Windows 2000 e dai sistemi che eseguono Internet Explorer 4.01. Se questa proprietà non è impostata, il programma di installazione ha il comportamento predefinito di creazione di funzionalità non annunciate durante l'installazione, in locale o in esecuzione dall'origine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Supporto della piattaforma dell'annuncio](platform-support-of-advertisement.md)
</dt> </dl>

 

 
