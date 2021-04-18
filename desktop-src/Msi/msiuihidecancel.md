---
description: Questa proprietà Windows Installer indica quando il livello dell'interfaccia utente interna è stato impostato per nascondere il pulsante Annulla.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Proprietà MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331073"
---
# <a name="msiuihidecancel-property"></a>Proprietà MsiUIHideCancel

Il programma di installazione imposta la proprietà **MsiUIHideCancel** su 1 quando il livello dell'interfaccia utente interna è stato impostato in modo da includere INSTALLUILEVEL \_ HIDECANCEL con la funzione [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la proprietà [UILevel](installer-uilevel.md)dell'oggetto del [**programma di installazione**](installer-object.md) o tramite opzioni della [riga di comando](command-line-options.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




