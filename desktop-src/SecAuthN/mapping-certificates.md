---
description: Mapping dei certificati
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapping dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758258"
---
# <a name="mapping-certificates"></a>Mapping dei certificati

> [!Note]  
> Le informazioni contenute in questo argomento sono valide solo per i server che richiedono l'autenticazione client.

 

Quando un'applicazione server richiede l'autenticazione client, Schannel prova automaticamente a eseguire il mapping del certificato fornito dal client a un account utente.

Una volta stabilito il [*contesto di sicurezza*](../secgloss/s-gly.md) , l'applicazione server può utilizzare la funzione [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) per ottenere un [*token di accesso*](../secgloss/a-gly.md) per l'account utente a cui è stato eseguito il mapping del [*certificato client*](../secgloss/c-gly.md) . Inoltre, il server può utilizzare la funzione [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) per rappresentare il client.

Per ulteriori informazioni sull'autenticazione, vedere [esecuzione dell'autenticazione tramite Schannel](performing-authentication-using-schannel.md).

 

 
