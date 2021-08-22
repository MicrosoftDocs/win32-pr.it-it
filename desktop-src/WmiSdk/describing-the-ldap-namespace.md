---
description: Quando ci si connette in remoto a un server Active Directory diverso da quello nel dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente ad Active Directory desiderato.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descrizione dello spazio dei nomi LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad19ea98e5bd6f36ff78159bfe0a106f0772921c152aa167c38e435732188446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568621"
---
# <a name="describing-the-ldap-namespace"></a>Descrizione dello spazio dei nomi LDAP

Quando ci si connette in remoto a un server Active Directory diverso da quello nel dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente ad Active Directory desiderato.

Per connettersi in remoto a un computer che è già membro del dominio appartenente al server Active Directory, digitare il comando seguente.

**\\\\Directory radice RemoteComputer \\ \\ \\ LDAP**

Questo esempio mostra che sono presenti due parti che costituiscono un nome di spazio dei nomi completo. La prima parte ( RemoteComputer) rappresenta il computer che è già membro del dominio \\ \\ appartenente al server Active Directory desiderato. La seconda parte ( \\ directory \\ radice \\ LDAP) rappresenta lo schema di Active Directory nel provider di servizi directory.

> [!Note]  
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

 

 



