---
description: Un trustee è l'account utente, il gruppo o la sessione di accesso a cui si applica una voce di controllo di accesso (ACE). Ogni voce ACE in un elenco di controllo di accesso (ACL) dispone di un ID di sicurezza (SID) che identifica un trustee.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Amministratori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234173"
---
# <a name="trustees"></a>Amministratori

Un trustee è l'account utente, il gruppo o la [*sessione di accesso*](/windows/desktop/SecGloss/l-gly) a cui si applica una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE). Ogni voce ACE in un [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) dispone di un ID di [*sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identifica un trustee.

Gli account utente includono gli account utilizzati da utenti o programmi, ad esempio i servizi Windows, per accedere al computer locale.

Gli account di gruppo non possono essere utilizzati per accedere a un computer, ma sono utili in ACE per consentire o negare un set di diritti di accesso a uno o più account utente.

Un [*SID di accesso*](/windows/desktop/SecGloss/l-gly) che identifica la sessione di accesso corrente è utile per consentire o negare i diritti di accesso solo fino a quando l'utente non si disconnette.

Le funzioni di controllo di accesso usano la struttura [**trustee**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) per identificare un trustee. La struttura **trustee** consente di usare una stringa del nome o un SID per identificare un trustee. Se si usa un nome, le funzioni che creano una voce ACE dalla struttura del **trustee** eseguono l'operazione di allocazione dei buffer SID e cercano il SID che corrisponde al nome dell'account. Sono disponibili due funzioni helper, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) e [**BuildTrusteeWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea), che inizializzano una struttura di **trustee** con un SID o un nome specificato. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) e [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) consentono di inizializzare una struttura del **trustee** con informazioni ACE specifiche dell'oggetto. Altre tre funzioni helper, [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma), [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)e [**GetTrusteeType**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea), recuperano i valori dei diversi membri di una struttura **trustee** .

Il membro **ptstrName** della struttura [**trustee**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) può essere un puntatore a un [**oggetto e a un \_ \_ nome**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) , a oggetti e a una struttura [**\_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) . Queste strutture specificano informazioni su una [voce ACE specifica dell'oggetto,](object-specific-aces.md) oltre a un nome o a un SID attendibile. In questo modo, le funzioni quali [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) e [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) consentono di archiviare informazioni ACE specifiche dell'oggetto nel membro del **trustee** della struttura di [**\_ accesso esplicita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) .

 

 
