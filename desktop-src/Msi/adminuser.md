---
description: Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Proprietà AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333678"
---
# <a name="adminuser-property"></a>Proprietà AdminUser

Il programma di installazione imposta questa proprietà se l'utente dispone di privilegi di amministratore.

**Windows Server 2008 e Windows Vista:** La proprietà **AdminUser** è uguale alla proprietà [**Privileged**](privileged.md) . Gli autori devono utilizzare la proprietà **Privileged** . Queste proprietà vengono impostate dal programma di installazione se l'utente dispone dei privilegi di amministratore, se l'applicazione è stata assegnata da un amministratore di sistema o se i criteri utente e computer AlwaysInstallElevated sono impostati su true.

## <a name="remarks"></a>Commenti

È possibile che le differenze tra queste proprietà siano state utilizzate in alcuni pacchetti legacy. Ad esempio, è possibile che sia stato usato **AdminUser** anziché [**Privileged**](privileged.md) nelle istruzioni condizionali, perché il programma di installazione imposta solo la proprietà **AdminUser** se l'utente è un amministratore. Il programma di installazione imposta la proprietà **Privileged** se l'utente è un amministratore o se Policy consente all'utente di eseguire l'installazione con privilegi elevati.

**Windows Server 2008 e Windows Vista:** Non supportato. [**Privileged**](privileged.md) e **AdminUser** sono uguali. I pacchetti che richiedono proprietà con **privilegi** e **AdminUser** distinti possono ripristinare la differenza impostando la proprietà [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .

Per ulteriori informazioni, vedere [installazione di un pacchetto con privilegi elevati per una proprietà non amministratore](installing-a-package-with-elevated-privileges-for-a-non-admin.md)e [**privilegiata**](privileged.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Vista o Windows Server 2008. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




