---
description: Il programma di installazione imposta questa proprietà se l'utente ha privilegi di amministratore.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b765aa4ece1bc19b5ed59e97a98ca4579042d52d65c0024ae018c794f9aaa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581911"
---
# <a name="adminuser-property"></a>AdminUser - proprietà

Il programma di installazione imposta questa proprietà se l'utente ha privilegi di amministratore.

**Windows Server 2008 e Windows Vista:** La **proprietà AdminUser** corrisponde alla [**proprietà Privileged.**](privileged.md) Gli autori devono usare **la proprietà Privileged.** Il programma di installazione imposta queste proprietà se l'utente dispone di privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.

## <a name="remarks"></a>Commenti

Le differenze tra queste proprietà potrebbero essere state usate in alcuni pacchetti legacy. Ad esempio, è possibile che sia stato usato **AdminUser** invece di [**Privileged**](privileged.md) nelle istruzioni condizionali, perché il programma di installazione imposta la proprietà **AdminUser** solo se l'utente è un amministratore. Il programma di installazione imposta **la proprietà Privileged** se l'utente è un amministratore o se i criteri consentono all'utente di installare con privilegi elevati.

**Windows Server 2008 e Windows Vista:** Non supportato. Privileged [**e**](privileged.md) **AdminUser** sono uguali. I pacchetti che richiedono **proprietà Privileged** e **AdminUser** distinte possono ripristinare la differenza impostando la [**proprietà MSIUSEREALADMINDETECTION.**](msiuserealadmindetection.md)

Per altre informazioni, vedere [Installazione di](installing-a-package-with-elevated-privileges-for-a-non-admin.md)un pacchetto con privilegi elevati per una proprietà senza privilegi di amministratore e [**Privileged.**](privileged.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Vista o Windows Server 2008. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




