---
description: I criteri ticket Kerberos vengono definiti a livello di dominio e implementati dall'Centro distribuzione chiavi (KDC) del dominio.
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Criteri Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d1dd394c42028c70f560fcb7f83b42bab506fbd222f877857be362a450041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127311"
---
# <a name="kerberos-policy"></a>Criteri Kerberos

I criteri ticket Kerberos vengono definiti a livello di dominio e implementati dal Centro distribuzione chiavi (KDC) [*del*](../secgloss/k-gly.md) dominio. I criteri Kerberos vengono archiviati in Active Directory come subset degli attributi dei criteri di sicurezza del dominio. Per impostazione predefinita, le opzioni dei criteri possono essere impostate solo dai membri del gruppo Domain Administrators. I criteri di dominio includono opzioni che:

-   Supporto dei ticket postdatati
-   Supporto della delega vincolata (Windows Solo Server 2003)
-   Ticket di supporto che possono essere inoltrati
-   Supportare i ticket per la produzione di energia elettrica
-   Impostare la validità massima del ticket
-   Impostare la durata massima del rinnovo
-   Impostare la validità massima del ticket proxy
-   Disconnettere forzatamente gli utenti alla scadenza dei ticket

Con [*la delega vincolata*](../secgloss/c-gly.md)è possibile impostare un computer per consentire l'inoltro delle credenziali solo a un elenco specifico di servizi. Tali servizi devono risiedere nello stesso dominio del computer che inoltra le credenziali. In *caso di delega* vincolata, i ticket non vengono più inviati dal client al server. Il computer server crea ticket di servizio da inoltrare in base alle esigenze dalle informazioni usate per autenticare il client.

Anche se i criteri Kerberos per un dominio possono consentire l'autenticazione delegata consentendo l'inoltro dei ticket, tale aspetto dei criteri non deve essere applicato a tutti gli utenti o a tutti i computer. È possibile impostare un attributo di un singolo account utente per disabilitare l'inoltro delle credenziali dell'utente [*da*](../secgloss/c-gly.md) parte di qualsiasi server. È possibile impostare un attributo dell'account di un singolo computer per disabilitare l'inoltro delle credenziali da qualsiasi utente. In entrambi i casi, la delega può essere disabilitata creando criteri di gruppo da applicare a tutti gli utenti o a tutti i computer in un'unità organizzativa di Active Directory.

**Windows XP/2000:** La delega vincolata non è supportata.

 

 
