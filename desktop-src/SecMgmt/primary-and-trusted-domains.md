---
description: I termini seguenti descrivono i domini presenti nei sistemi remoti.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domini primari e Trusted
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525717"
---
# <a name="primary-and-trusted-domains"></a>Domini primari e Trusted

I termini seguenti descrivono i domini presenti nei sistemi remoti.

-   [Dominio primario](#primary-domain)
-   [Dominio trusted](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Dominio primario

Un dominio primario è il dominio responsabile della creazione di relazioni di trust aggiuntive e l'esecuzione dell'autenticazione (o per il passaggio di una richiesta di autenticazione a un dominio trusted appropriato). I controller di dominio nel dominio primario gestiscono o passano le richieste di autenticazione che provengono dalla workstation.

Quando si verifica l'accesso, LSA controlla i domini di account e predefiniti per le informazioni di autenticazione. Se l'account a cui si è connessi non è in uno di questi domini, la richiesta di accesso viene passata al dominio primario del sistema.

## <a name="trusted-domain"></a>Dominio trusted

Un dominio trusted è un dominio considerato attendibile dal sistema locale per autenticare gli utenti. In altre parole, se un utente o un'applicazione viene autenticata da un dominio trusted, questa autenticazione viene accettata da tutti i domini che considerano attendibile il dominio di autenticazione.

Ogni dominio subordinato dispone automaticamente di una relazione di trust bidirezionale con il dominio principale. Per impostazione predefinita, questa relazione di trust è transitiva, vale a dire che se un sistema considera attendibile il dominio A, considera attendibili anche tutti i domini A cui viene associato un trust. I trust unidirezionali sono supportati anche per i sistemi operativi precedenti a Windows 2000, che non supportano i trust transitivi bidirezionali.

L' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) ha un tipo di oggetto, [**trustedDomain**](the-trusteddomain-object-type.md), usato per archiviare le informazioni sulle relazioni di trust, inclusi il nome e l' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) del dominio trusted, l'account nel dominio da usare per le richieste di autenticazione, le richieste di conversione di nome e SID e i nomi dei controller di dominio nel dominio trusted.

Nei controller di dominio, LSA crea un'istanza di un oggetto [**trustedDomain**](the-trusteddomain-object-type.md) per ogni dominio considerato attendibile dal sistema locale.

Se, ad esempio, una workstation Windows XP considera attendibile un controller di dominio di Windows 2000 che a sua volta considera attendibili altri quattro sistemi, la workstation, connessa con attendibilità transitiva, avrà cinque oggetti [**trustedDomain**](the-trusteddomain-object-type.md) nel sistema locale.

 

 
