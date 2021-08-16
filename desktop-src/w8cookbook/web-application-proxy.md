---
title: Proxy applicazione Web
description: Proxy applicazione Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211326"
---
# <a name="web-application-proxy"></a>Proxy applicazione Web

## <a name="platform"></a>Piattaforma

**Server -** Windows Server 2012 R2  






## <a name="description"></a>Descrizione

In Windows Server 2012 R2 è stato aggiunto un nuovo servizio denominato Web Application Proxy con il ruolo Accesso remoto che consente agli amministratori di pubblicare applicazioni per l'accesso esterno. Questo servizio funge da proxy inverso e come proxy Active Directory Federation Services (AD FS). In realtà, questo servizio sostituisce il AD FS proxy come era noto in Windows Server 2012.

Con l'Application Proxy Web, un'organizzazione può rendere disponibili le risorse Web locali per l'accesso esterno, gestendo al tempo stesso il rischio di questo accesso controllando i criteri di autenticazione e autorizzazione nel AD FS.

## <a name="manifestation"></a>Manifestazione

Il AD FS proxy non è più nel ruolo Active Directory Federation Services (AD FS), ma è stato sostituito dal Application Proxy Web nel ruolo Accesso remoto. Rappresenta un'espansione del servizio proxy AD FS includendo la funzionalità del proxy inverso per la pubblicazione dell'applicazione.

## <a name="solution"></a>Soluzione

Per accedere all'Application Proxy Web, gli amministratori possono passare a Server Manager e aggiungere un nuovo ruolo o un nuovo servizio ruolo. L'amministratore troverà l'Application Proxy Web nel ruolo Accesso remoto.

## <a name="resources"></a>Risorse

-   [Guida alla soluzione](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 