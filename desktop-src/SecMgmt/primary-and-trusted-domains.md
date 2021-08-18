---
description: I termini seguenti descrivono i domini esistenti nei sistemi remoti.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domini primari e trusted
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80f1bd4983a17725de1bac9c55aae0f7d64e85bc2768bfaea2ca1469ed3d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005065"
---
# <a name="primary-and-trusted-domains"></a>Domini primari e trusted

I termini seguenti descrivono i domini esistenti nei sistemi remoti.

-   [Dominio primario](#primary-domain)
-   [Dominio trusted](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Dominio primario

Un dominio primario è il dominio responsabile della definizione di ulteriori relazioni di trust e dell'esecuzione dell'autenticazione (o del passaggio di una richiesta di autenticazione a un dominio trusted appropriato). I controller di dominio nel dominio primario gestiscono o passano le richieste di autenticazione che hanno origine nella workstation.

Quando si verifica l'accesso, l'account LSA controlla le informazioni di autenticazione nei domini predefiniti e dell'account. Se l'account a cui si è connessi non si trova in uno di questi domini, la richiesta di accesso viene inviata al dominio primario del sistema.

## <a name="trusted-domain"></a>Dominio trusted

Un dominio trusted è un dominio considerato attendibile dal sistema locale per autenticare gli utenti. In altre parole, se un utente o un'applicazione viene autenticata da un dominio trusted, questa autenticazione viene accettata da tutti i domini che considera attendibile il dominio di autenticazione.

Ogni dominio subordinato ha automaticamente una relazione di trust bidirezionale con il dominio principale. Per impostazione predefinita, questo trust è transitivo, vale a dire che se un sistema considera attendibile il dominio A, considera attendibili anche tutti i domini che il dominio A considera attendibili. I trust unidirezionale sono supportati anche per i sistemi operativi precedenti Windows 2000, che non supportano i trust transitivi bidirezionale.

L'autorità di sicurezza locale [](/windows/desktop/SecGloss/l-gly) (LSA) ha un tipo di oggetto, [**TrustedDomain**](the-trusteddomain-object-type.md), usato per archiviare informazioni sulle relazioni di trust, inclusi il nome e l'ID di sicurezza [](/windows/desktop/SecGloss/s-gly) (SID) del dominio trusted, l'account nel dominio da usare per le richieste di autenticazione, le richieste di conversione di nomi e SID e i nomi dei controller di dominio nel dominio trusted.

Nei controller di dominio, LSA crea un'istanza di un [**oggetto TrustedDomain**](the-trusteddomain-object-type.md) per ogni dominio considerato attendibile dal sistema locale.

Ad esempio, se una workstation di Windows XP considera attendibile un controller di dominio di Windows 2000 che a sua volta considera attendibile altri quattro sistemi, la workstation connessa tramite trust transitivo avrà cinque oggetti [**TrustedDomain**](the-trusteddomain-object-type.md) nel sistema locale.

 

 
