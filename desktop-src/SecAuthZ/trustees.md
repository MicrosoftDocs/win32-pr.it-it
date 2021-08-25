---
description: Un fiduciare è l'account utente, l'account di gruppo o la sessione di accesso a cui si applica una voce di controllo di accesso (ACE). Ogni voce ACE in un elenco di controllo di accesso (ACL) ha un identificatore di sicurezza (SID) che identifica un fiduciare.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Fiduciari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e79bc49a4ffc93c87b040327a2c7626bc7d816e060cf4bfcd42a6bcab0d024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906961"
---
# <a name="trustees"></a>Fiduciari

Un fiduciare è l'account utente, [](/windows/desktop/SecGloss/l-gly) l'account di gruppo o la sessione di accesso a cui si applica una voce di controllo di accesso [](/windows/desktop/SecGloss/a-gly) (ACE). Ogni voce ACE in un elenco di [*controllo*](/windows/desktop/SecGloss/a-gly) di accesso [](/windows/desktop/SecGloss/s-gly) (ACL) ha un identificatore di sicurezza (SID) che identifica un fiduciare.

Gli account utente includono gli account che utenti o programmi, ad esempio Windows Services, usano per accedere al computer locale.

Gli account di gruppo non possono essere usati per accedere a un computer, ma sono utili nelle voci ACE per consentire o negare un set di diritti di accesso a uno o più account utente.

Un [*SID di accesso*](/windows/desktop/SecGloss/l-gly) che identifica la sessione di accesso corrente è utile per consentire o negare i diritti di accesso solo fino a quando l'utente non si disconnette.

Le funzioni di controllo di accesso usano la [**struttura TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) per identificare un fiduciare. La **struttura TRUSTEE** consente di usare una stringa del nome o un SID per identificare un fiduciare. Se si usa un nome, le funzioni che creano una ACE dalla struttura **TRUSTEE** eseguono l'attività di allocazione dei buffer SID e ricerca del SID corrispondente al nome dell'account. Sono disponibili due funzioni helper, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) e [**BuildTrusteeWithName,**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea)che inizializzano una struttura **TRUSTEE** con un SID o un nome specificato. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) e [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) consentono di inizializzare una struttura **TRUSTEE** con informazioni ACE specifiche dell'oggetto. Altre tre funzioni helper, [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma), [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)e [**GetTrusteeType**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea), recuperano i valori dei vari membri di una **struttura TRUSTEE.**

Il **membro ptstrName** della struttura [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) può essere un puntatore a una struttura [**OBJECTS AND \_ \_ NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) [**o OBJECTS AND \_ \_ SID.**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) Queste strutture specificano informazioni su una [ACE specifica](object-specific-aces.md) dell'oggetto oltre a un nome fiduciare o un SID. Ciò consente a funzioni come [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) e [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) di archiviare le informazioni ACE specifiche dell'oggetto nel membro **Trustee** della struttura [**EXPLICIT \_ ACCESS.**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)

 

 
