---
description: Il programma di installazione imposta il valore della proprietà MsiRestartManagerSessionKey sulla chiave di sessione per la sessione di gestione riavvio.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Proprietà MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331081"
---
# <a name="msirestartmanagersessionkey-property"></a>Proprietà MsiRestartManagerSessionKey

Il programma di installazione imposta il valore della proprietà **MsiRestartManagerSessionKey** sulla chiave di sessione per la sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) . Le azioni personalizzate possono utilizzare la chiave della sessione per partecipare alla sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) .

## <a name="remarks"></a>Commenti

Il programma di installazione imposta il valore della proprietà **MsiRestartManagerSessionKey** in fase di inizializzazione, quindi cancella il valore durante l'azione [InstallValidate](installvalidate-action.md) . Le azioni personalizzate che richiedono il valore della proprietà **MsiRestartManagerSessionKey** devono essere precedenti all'azione InstallValidate nella sequenza di azione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
