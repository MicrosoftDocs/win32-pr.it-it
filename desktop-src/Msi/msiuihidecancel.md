---
description: Questa Windows installer indica quando il livello di interfaccia utente interno è stato impostato per nascondere il pulsante Annulla.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: MsiUIHideCancel - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da3c0888ea760e7e8627710b061112d350f94af569697b7ad0616d1dbacbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943989"
---
# <a name="msiuihidecancel-property"></a>MsiUIHideCancel - proprietà

Il programma di installazione imposta la proprietà **MsiUIHideCancel** su 1 quando il livello di interfaccia utente interno è stato impostato in modo da includere INSTALLUILEVEL HIDECANCEL con la funzione \_ [](command-line-options.md) [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la proprietà [UILevel](installer-uilevel.md)dell'oggetto [**Installer**](installer-object.md) o tramite le opzioni della riga di comando .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva Windows Server 2003 o Windows XP. Per informazioni Windows service pack minimo richiesto da una versione Windows Windows [Installer,](windows-installer-portal.md) vedere l'Windows installer Run-Time requisiti minimi.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




