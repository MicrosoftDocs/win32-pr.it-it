---
description: La proprietà Privileged indica se l'installazione viene eseguita nel contesto di privilegi elevati.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Proprietà Privileged
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332844"
---
# <a name="privileged-property"></a>Proprietà Privileged

La proprietà **Privileged** indica se l'installazione viene eseguita nel contesto di privilegi elevati. Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.

## <a name="default-value"></a>Valore predefinito

Il programma di installazione non imposta questa proprietà se l'utente non è autorizzato a eseguire l'installazione con privilegi elevati.

## <a name="remarks"></a>Commenti

Gli sviluppatori di pacchetti del programma di installazione possono utilizzare la proprietà **Privileged** per rendere l'installazione condizionale sui criteri di sistema, l'utente amministratore o l'assegnazione da parte di un amministratore.

Quando è in esecuzione in Windows Vista, i **privilegi** e [**AdminUser**](adminuser.md) sono gli stessi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




