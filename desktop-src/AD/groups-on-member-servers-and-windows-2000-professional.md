---
title: Gruppi su server membri e Windows 2000 Professional
description: Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è disponibile un database di sicurezza locale.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Gruppi su server membri e Windows 2000 Professional AD
- gruppi di Active Directory, gruppi su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328484"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Gruppi su server membri e Windows 2000 Professional

Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è disponibile un database di sicurezza locale. Questo database di sicurezza locale può contenere il proprio utente locale e i gruppi locali il cui ambito è solo il computer in cui sono stati creati. Quando si gestiscono questi tipi di utenti e gruppi su server membri e computer in cui è in esecuzione la workstation Windows NT o Windows 2000 Professional, utilizzare il provider WinNT.

Quando un server membro o un computer in cui è in esecuzione Windows 2000 Professional o Windows 2000 Professional è membro di un dominio Windows 2000, i gruppi o gli utenti del dominio possono essere utilizzati nel database di sicurezza locale per concedere diritti a tale gruppo in quel particolare computer.

Quando si gestiscono i gruppi in un dominio Windows 2000 usando ADSI, usare il provider LDAP. Quando si gestiscono gruppi su server membri e computer in cui è in esecuzione la workstation Windows NT o Windows 2000 Professional, utilizzare il provider WinNT.

È necessario associare almeno un'istanza a ogni provider: 1) eseguire l'associazione al provider LDAP per recuperare ADsPath al gruppo o all'utente che si desidera aggiungere a un gruppo nel database locale e 2) eseguire l'associazione al provider WinNT per aggiungere tale utente o gruppo a un gruppo locale.

 

 




