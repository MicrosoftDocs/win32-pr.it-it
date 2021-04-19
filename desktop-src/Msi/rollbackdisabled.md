---
description: Il programma di installazione imposta la proprietà RollbackDisabled quando il rollback è stato disabilitato.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Proprietà RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326371"
---
# <a name="rollbackdisabled-property"></a>Proprietà RollbackDisabled

Il programma di installazione imposta la proprietà **RollbackDisabled** quando il rollback è stato disabilitato. **RollbackDisabled** viene usato dagli autori di pacchetti che devono assicurarsi che il programma di installazione non abbia disabilitato il rollback. La proprietà **RollbackDisabled** può essere utilizzata in un'espressione condizionale che rifiuta di continuare con l'installazione se è impostata la proprietà **RollbackDisabled** .

## <a name="default-value"></a>Valore predefinito

Per impostazione predefinita, il rollback è abilitato.

## <a name="remarks"></a>Commenti

Poiché [rollback](rollback-custom-actions.md) e [commit](commit-custom-actions.md) non vengono eseguiti mentre il rollback è disabilitato, il programma di installazione non è in grado di installare correttamente un pacchetto che utilizza questi tipi di azioni personalizzate in una transazione durante l'installazione. In questo caso, l'autore del pacchetto deve includere una condizione che usa DisableRollback che impedisce l'installazione di continuare se il rollback è disabilitato.

Il valore del criterio DisableRollback può essere impostato da un amministratore come parte dell'assegnazione di criteri di sistema. Si consiglia agli amministratori di non disabilitare il rollback a meno che non sia necessario. Per ulteriori informazioni sul valore del criterio DisableRollback, vedere [criteri di sistema](system-policy.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Rollback dell'installazione](rollback-installation.md)
</dt> <dt>

[Criteri di sistema](system-policy.md)
</dt> <dt>

[rollback delle azioni personalizzate](rollback-custom-actions.md)
</dt> <dt>

[Esegui commit di azioni personalizzate](commit-custom-actions.md)
</dt> </dl>

 

 




