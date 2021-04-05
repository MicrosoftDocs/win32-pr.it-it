---
description: Quando ci si connette in remoto a un server Active Directory diverso da quello del dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente al Active Directory desiderato.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descrizione dello spazio dei nomi LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058018"
---
# <a name="describing-the-ldap-namespace"></a>Descrizione dello spazio dei nomi LDAP

Quando ci si connette in remoto a un server Active Directory diverso da quello del dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente al Active Directory desiderato.

Per connettersi in remoto a un computer che è già membro del dominio appartenente al server Active Directory, digitare il comando seguente.

**\\\\ComputerRemoto \\ \\ directory radice \\ LDAP**

Questo esempio mostra che sono presenti due parti che costituiscono un nome completo dello spazio dei nomi. La prima parte ( \\ \\ ComputerRemoto) rappresenta il computer che è già membro del dominio appartenente al server Active Directory desiderato. La seconda parte ( \\ \\ directory radice \\ LDAP) rappresenta lo schema Active Directory nel provider dei servizi directory.

> [!Note]  
> Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

 

 

 



