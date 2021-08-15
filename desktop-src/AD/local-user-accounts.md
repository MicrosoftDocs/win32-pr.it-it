---
title: Uso di un account utente locale come account di accesso al servizio
description: Un account utente locale (formato nome \ 0034;. \\ UserName \ 0034;) esiste solo nel database SAM del computer host. non dispone di un oggetto utente in Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186856"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Uso di un account utente locale come account di accesso al servizio

Un account utente locale (formato nome: ". \\ *UserName*") esiste solo nel database SAM del computer host. non dispone di un oggetto utente in Active Directory Domain Services. Ciò significa che un account locale non può essere autenticato dal dominio. Di conseguenza, un servizio eseguito nel contesto di sicurezza di un account utente locale non ha accesso alle risorse di rete (tranne che come utente anonimo) e non può supportare l'autenticazione reciproca Kerberos in cui il servizio viene autenticato dai client. Per questi motivi, gli account utente locali non sono in genere appropriati per i servizi abilitati per la directory. Sul lato positivo, i bug nel servizio non possono danneggiare il sistema. Se il servizio può essere eseguito in base a tali limitazioni, dovrebbe.

 

 




