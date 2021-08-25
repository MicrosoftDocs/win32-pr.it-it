---
description: Il programma di installazione imposta il valore della proprietà UserSID sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione. Per altre informazioni, vedere Strutture di autorizzazione.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809161"
---
# <a name="usersid-property"></a>UserSID - proprietà

Il programma di installazione imposta il valore **della proprietà UserSID** sulla rappresentazione di stringa dell'ID di sicurezza (SID) dell'utente che esegue l'installazione. Per altre informazioni, vedere [Strutture di autorizzazione.](../secauthz/authorization-structures.md)

## <a name="default-value"></a>Valore predefinito

No.

## <a name="remarks"></a>Osservazioni

Il Windows programma di installazione di Windows imposta questa proprietà Windows 2000, Windows XP e Windows Vista. Questa proprietà non è definita in tutti gli altri sistemi operativi.

Si noti che questa proprietà ha l'attributo speciale che può essere recuperato da un'azione personalizzata posticipata. Un'azione personalizzata in esecuzione con privilegi elevati può comunque restituire il SID dell'utente nella **proprietà UserSID.** Per informazioni, vedere [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
