---
description: La proprietà Privileged indica se l'installazione viene eseguita nel contesto dei privilegi elevati.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Proprietà con privilegi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe61f17e5ef3453021c98bac8eb383171a678adfb204886ecdaa840e0df832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129131"
---
# <a name="privileged-property"></a>Proprietà con privilegi

La **proprietà Privileged** indica se l'installazione viene eseguita nel contesto dei privilegi elevati. Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.

## <a name="default-value"></a>Valore predefinito

Il programma di installazione non imposta questa proprietà se l'utente non è autorizzato a eseguire l'installazione con privilegi elevati.

## <a name="remarks"></a>Commenti

Gli sviluppatori di pacchetti del programma di installazione possono usare la proprietà **Privileged** per rendere l'installazione condizionale in base ai criteri di sistema, all'utente amministratore o all'assegnazione da parte di un amministratore.

Quando si esegue Windows Vista, **Privileged** e [**AdminUser**](adminuser.md) sono uguali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




