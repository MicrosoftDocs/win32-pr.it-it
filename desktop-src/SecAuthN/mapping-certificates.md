---
description: Mapping dei certificati
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapping dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f671afa6278da49427d0f7b49f78895198333e24d135383207b359846216638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921840"
---
# <a name="mapping-certificates"></a>Mapping dei certificati

> [!Note]  
> Le informazioni contenute in questo argomento sono valide solo per i server che richiedono l'autenticazione client.

 

Quando un'applicazione server richiede l'autenticazione client, Schannel prova automaticamente a eseguire il mapping del certificato fornito dal client a un account utente.

Dopo aver [*stabilito il contesto*](../secgloss/s-gly.md) di sicurezza, l'applicazione server può usare la funzione [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) per ottenere un [*token*](../secgloss/a-gly.md) di accesso per l'account utente a cui è stato eseguito il mapping del certificato [*client.*](../secgloss/c-gly.md) Inoltre, il server può usare la [**funzione ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) per rappresentare il client.

Per altre informazioni sull'autenticazione, vedere [Esecuzione dell'autenticazione tramite Schannel.](performing-authentication-using-schannel.md)

 

 
