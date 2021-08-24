---
description: Il programma di installazione imposta la proprietà RollbackDisabled quando il rollback è stato disabilitato.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: RollbackDisabled - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df5b392a69a04811853a449106858445969fed3b2c0598266ff3f8a1bcb51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039871"
---
# <a name="rollbackdisabled-property"></a>RollbackDisabled - proprietà

Il programma di installazione imposta la **proprietà RollbackDisabled** quando il rollback è stato disabilitato. **RollbackDisabled viene** usato dagli autori di pacchetti che devono assicurarsi che il programma di installazione non abbia disabilitato il rollback. La **proprietà RollbackDisabled** può essere usata in un'espressione condizionale che in effetti rifiuta di continuare l'installazione se è impostata la proprietà **RollbackDisabled.**

## <a name="default-value"></a>Valore predefinito

Per impostazione predefinita, il rollback è abilitato.

## <a name="remarks"></a>Commenti

Poiché [il rollback e](rollback-custom-actions.md) il [commit](commit-custom-actions.md) non vengono eseguiti mentre il rollback è disabilitato, il programma di installazione non può installare correttamente un pacchetto che utilizza questi tipi di azioni personalizzate in una transazione durante l'installazione. In questo caso, l'autore del pacchetto deve includere una condizione che usa DisableRollback che impedisce la continuazione dell'installazione se il rollback è disabilitato.

Il valore del criterio DisableRollback può essere impostato da un amministratore come parte dell'assegnazione dei criteri di sistema. È consigliabile che gli amministratori non disabilitino il rollback a meno che non sia necessario. Per altre informazioni sul valore dei criteri DisableRollback, vedere Criteri [di sistema.](system-policy.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Rollback dell'installazione](rollback-installation.md)
</dt> <dt>

[Criteri di sistema](system-policy.md)
</dt> <dt>

[rollback di azioni personalizzate](rollback-custom-actions.md)
</dt> <dt>

[eseguire il commit di azioni personalizzate](commit-custom-actions.md)
</dt> </dl>

 

 




