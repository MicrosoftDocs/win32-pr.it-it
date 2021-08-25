---
description: Un descrittore di sicurezza contiene le informazioni di sicurezza associate a un oggetto a protezione diretta.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descrittori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1049becf755bbb0940cfd5def3b59662a20eb2a690d90a36e06c5706212f02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907191"
---
# <a name="security-descriptors"></a>Descrittori di sicurezza

Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) contiene le informazioni di sicurezza associate a un oggetto a protezione [diretta.](securable-objects.md) Un descrittore di sicurezza è costituito da una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e dalle informazioni di sicurezza associate. Un descrittore di sicurezza può includere le informazioni di sicurezza seguenti:

-   [ID di sicurezza](security-identifiers.md) (SID) per il proprietario e il gruppo primario di un oggetto.
-   Elenco [DACL](access-control-lists.md) che specifica i diritti di accesso consentiti o negati a utenti o gruppi specifici.
-   SaCL [che](access-control-lists.md) specifica i tipi di tentativi di accesso che generano record di controllo per l'oggetto.
-   Set di bit di controllo che qualificano il significato di un descrittore di sicurezza o dei relativi singoli membri.

Le applicazioni non devono modificare direttamente il contenuto di un descrittore di sicurezza. L Windows API fornisce funzioni per l'impostazione e il recupero delle informazioni di sicurezza nel descrittore di sicurezza di un oggetto. Sono inoltre disponibili funzioni per la creazione e l'inizializzazione di un descrittore di sicurezza per un nuovo oggetto.

Le applicazioni che usano descrittori di sicurezza su oggetti Active Directory possono usare le funzioni di sicurezza Windows o le interfacce di sicurezza fornite da Active Directory Service Interfaces (ADSI). Per altre informazioni sulle interfacce di sicurezza ADSI, vedere [Funzionamento del controllo di accesso in Active Directory.](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services)

 

 
