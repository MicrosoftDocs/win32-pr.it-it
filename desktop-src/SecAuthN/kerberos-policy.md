---
description: I criteri del ticket Kerberos vengono definiti a livello di dominio e implementati dal Centro distribuzione chiavi del dominio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Criteri Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313294"
---
# <a name="kerberos-policy"></a>Criteri Kerberos

I criteri del ticket Kerberos vengono definiti a livello di dominio e implementati dal [*centro distribuzione chiavi*](../secgloss/k-gly.md) del dominio (KDC). Il criterio Kerberos viene archiviato nel Active Directory come un subset degli attributi dei criteri di sicurezza del dominio. Per impostazione predefinita, le opzioni dei criteri possono essere impostate solo dai membri del gruppo Domain Administrators. I criteri di dominio includono opzioni che:

-   Supporto per ticket aggiornati
-   Supporto della delega vincolata (solo Windows Server 2003)
-   Ticket di supporto che possono essere trasmessi
-   Supporto di ticket rinnovabili
-   Imposta validità massima ticket
-   Imposta validità massima del rinnovo
-   Imposta validità massima ticket proxy
-   Disconnettere forzatamente gli utenti quando i ticket scadono

Con la [*delega vincolata*](../secgloss/c-gly.md)è possibile impostare un computer in modo da consentire l'invio delle credenziali solo a un elenco specifico di servizi. Tali servizi devono trovarsi nello stesso dominio del computer che invia le credenziali. In *delega vincolata*, i ticket non vengono più inviati dal client al server. Il computer server crea ticket di servizio da inviare in base alle informazioni necessarie per autenticare il client.

Sebbene i criteri Kerberos per un dominio consentano l'autenticazione delegata consentendo l'invio dei ticket, l'aspetto del criterio non deve essere applicato a tutti gli utenti o a tutti i computer. Un attributo di un singolo account utente può essere impostato in modo da disabilitare l'invio delle [*credenziali*](../secgloss/c-gly.md) dell'utente da qualsiasi server. È possibile impostare un attributo dell'account di un singolo computer per disabilitare l'invio di credenziali da qualsiasi utente. In entrambi i casi, è possibile disabilitare la delega creando un criterio di gruppo da applicare a tutti gli utenti o a tutti i computer in un'unità organizzativa del Active Directory.

**Windows XP/2000:** La delega vincolata non è supportata.

 

 
