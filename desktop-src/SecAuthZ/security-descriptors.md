---
description: Un descrittore di sicurezza contiene le informazioni di sicurezza associate a un oggetto a protezione diretta.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descrittori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879650"
---
# <a name="security-descriptors"></a>Descrittori di sicurezza

Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) contiene le informazioni di sicurezza associate a un [oggetto a protezione diretta](securable-objects.md). Un descrittore di sicurezza è costituito da una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e dalle informazioni di sicurezza Un descrittore di sicurezza può includere le informazioni di sicurezza seguenti:

-   [ID di sicurezza](security-identifiers.md) (SID) per il proprietario e il gruppo primario di un oggetto.
-   [Elenco DACL](access-control-lists.md) che specifica i diritti di accesso consentiti o negati a utenti o gruppi specifici.
-   [SACL](access-control-lists.md) che specifica i tipi di tentativi di accesso che generano record di controllo per l'oggetto.
-   Set di bit di controllo che qualificano il significato di un descrittore di sicurezza o dei singoli membri.

Le applicazioni non devono modificare direttamente il contenuto di un descrittore di sicurezza. L'API di Windows fornisce funzioni per l'impostazione e il recupero delle informazioni di sicurezza nel descrittore di sicurezza di un oggetto. Sono inoltre disponibili funzioni per la creazione e l'inizializzazione di un descrittore di sicurezza per un nuovo oggetto.

Le applicazioni che utilizzano descrittori di sicurezza su oggetti Active Directory possono utilizzare le funzioni di sicurezza di Windows o le interfacce di sicurezza fornite da Active Directory Service Interfaces (ADSI). Per ulteriori informazioni sulle interfacce di sicurezza ADSI, vedere funzionamento [del controllo di accesso in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
