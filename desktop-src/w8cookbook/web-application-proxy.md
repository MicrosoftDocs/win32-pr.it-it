---
title: Proxy applicazione Web
description: Proxy applicazione Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104118575"
---
# <a name="web-application-proxy"></a>Proxy applicazione Web

## <a name="platform"></a>Piattaforma

**Server-** Windows Server 2012 R2  






## <a name="description"></a>Descrizione

In Windows Server 2012 R2 è stato aggiunto un nuovo servizio denominato proxy applicazione Web con il ruolo accesso remoto che consente agli amministratori di pubblicare applicazioni per l'accesso esterno. Questo servizio funge da proxy inverso e come proxy di Active Directory Federation Services (AD FS). Questo servizio sostituisce infatti il servizio proxy AD FS come è noto in Windows Server 2012.

Con il proxy dell'applicazione Web, un'organizzazione può rendere disponibili risorse Web locali per l'accesso esterno, gestendo allo stesso tempo il rischio di questo accesso controllando i criteri di autenticazione e autorizzazione nel AD FS.

## <a name="manifestation"></a>Manifestazione

Il servizio proxy AD FS non è più sotto il ruolo di Active Directory Federation Services (AD FS), ma è stato sostituito dal proxy dell'applicazione Web nel ruolo accesso remoto. Rappresenta un'espansione del servizio proxy AD FS includendo la funzionalità del proxy inverso per la pubblicazione dell'applicazione.

## <a name="solution"></a>Soluzione

Per accedere al proxy dell'applicazione Web, gli amministratori possono passare a Server Manager e aggiungere un nuovo ruolo/servizio ruolo. L'amministratore troverà il proxy applicazione Web nel ruolo accesso remoto.

## <a name="resources"></a>Risorse

-   [Guida alla soluzione](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 