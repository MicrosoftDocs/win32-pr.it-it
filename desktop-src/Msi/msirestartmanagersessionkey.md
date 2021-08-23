---
description: Il programma di installazione imposta il valore della proprietà MsiRestartManagerSessionKey sulla chiave di sessione per la sessione di Gestione riavvio.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: MsiRestartManagerSessionKey - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f48fe8d2ce4b287afc5c222acdc1f71eec393ff9a1ab1773a822e30405e6a317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944539"
---
# <a name="msirestartmanagersessionkey-property"></a>MsiRestartManagerSessionKey - proprietà

Il programma di installazione imposta il valore della **proprietà MsiRestartManagerSessionKey** sulla chiave di sessione per la [sessione di Gestione riavvio.](../rstmgr/restart-manager-portal.md) Le azioni personalizzate possono usare la chiave di sessione per partecipare alla [sessione di Gestione riavvio.](../rstmgr/restart-manager-portal.md)

## <a name="remarks"></a>Commenti

Il programma di installazione imposta il valore della **proprietà MsiRestartManagerSessionKey** all'inizializzazione e quindi cancella il valore durante l'azione [InstallValidate.](installvalidate-action.md) Le azioni personalizzate che necessitano del valore della **proprietà MsiRestartManagerSessionKey** devono essere eseguite prima dell'azione InstallValidate nella sequenza di azioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Per informazioni Windows sul Service Pack minimo richiesto da una versione [Windows Installer,](windows-installer-portal.md) vedere l'Run-Time di installazione.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
