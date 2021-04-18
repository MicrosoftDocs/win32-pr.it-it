---
description: Il programma di installazione imposta il valore della proprietà UserSID sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione. Per altre informazioni, vedere strutture di autorizzazione.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: Proprietà UserSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328551"
---
# <a name="usersid-property"></a>Proprietà UserSID

Il programma di installazione imposta il valore della proprietà **UserSID** sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione. Per altre informazioni, vedere [strutture di autorizzazione](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Valore predefinito

No.

## <a name="remarks"></a>Osservazioni

Il Windows Installer impostare questa proprietà in Windows 2000, Windows XP e Windows Vista. Questa proprietà non è definita in tutti gli altri sistemi operativi.

Si noti che questa proprietà ha l'attributo speciale che può essere recuperato da un'azione personalizzata posticipata. Un'azione personalizzata eseguita con privilegi elevati può comunque restituire il SID dell'utente nella proprietà **UserSID** . Per informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
