---
description: La proprietà MSIRESTARTMANAGERCONTROL specifica se il pacchetto Windows Installer utilizza la funzionalità di gestione riavvio o della finestra di dialogo FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Proprietà MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331082"
---
# <a name="msirestartmanagercontrol-property"></a>Proprietà MSIRESTARTMANAGERCONTROL

La proprietà **MSIRESTARTMANAGERCONTROL** specifica se il pacchetto Windows Installer utilizza la funzionalità di [Gestione riavvio](../rstmgr/restart-manager-portal.md) o della [finestra di dialogo FilesInUse](filesinuse-dialog.md) .

## <a name="value"></a>Valore



| Valore                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Si tratta del valore predefinito se la proprietà non è impostata. Windows Installer tenta sempre di utilizzare [Gestione riavvio](../rstmgr/restart-manager-portal.md) in Windows Vista.<br/>                                                                                                                                                                                                       |
| <dl> <dt>Disabilitare</dt> </dl>         | Disabilita l'interazione del pacchetto con [Gestione riavvio](../rstmgr/restart-manager-portal.md). Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md). <br/>                                                                                                                                                                                                      |
| <dl> <dt>DisableShutdown</dt> </dl> | Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md). Questa impostazione Disabilita i tentativi da parte di [Gestione riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii durante l'installazione di un pacchetto di Windows Installer che non è stato creato per usare Gestione riavvio. Il programma di installazione utilizza ancora Gestione riavvio per rilevare i file utilizzati dalle applicazioni. <br/> |



 

## <a name="remarks"></a>Commenti

La proprietà **MSIRESTARTMANAGERCONTROL** viene ignorata se [Gestione riavvio](../rstmgr/restart-manager-portal.md) non è disponibile o è disabilitato.

Il valore di questa proprietà può essere modificato usando le trasformazioni di personalizzazione o gli aggiornamenti. La modifica del valore di questa proprietà da azioni personalizzate non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
