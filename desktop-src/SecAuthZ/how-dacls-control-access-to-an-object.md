---
description: Quando un thread tenta di accedere a un oggetto a protezione diretta, il sistema concede o nega l'accesso.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Funzionamento di AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c593c0c50fa1e78639d18bc5c2f372e9c0edd0690e9b338a5126794da54509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671971"
---
# <a name="how-accesscheck-works"></a>Funzionamento di AccessCheck

Quando un thread tenta di accedere a un oggetto a protezione diretta, il sistema concede o nega l'accesso. Se l'oggetto non dispone di un elenco di [*controllo*](/windows/desktop/SecGloss/d-gly) di accesso discrezionale (DACL), il sistema concede l'accesso; In caso contrario, il sistema cerca le voci di controllo di accesso [(ACE)](access-control-entries.md) nell'elenco DACL dell'oggetto che si applicano al thread. Ogni ACE nell'elenco DACL dell'oggetto specifica i diritti di accesso consentiti o negati per un [trustee,](trustees.md)che può essere un account utente, un account di gruppo o una sessione di [*accesso*](/windows/desktop/SecGloss/l-gly).

## <a name="dacls"></a>DACL

Il sistema confronta il trustee in ogni ACE con i trustee identificati nel token di accesso [del thread.](access-tokens.md) Un token di accesso [*contiene id di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identificano l'utente e gli account di gruppo a cui appartiene l'utente. Un token contiene anche un [*SID di accesso*](/windows/desktop/SecGloss/l-gly) che identifica la sessione di accesso corrente. Durante un controllo di accesso, il sistema ignora i SID di gruppo non abilitati. Per altre informazioni sui SID abilitati, disabilitati e di sola negazione, vedere [Attributi SID in un token di accesso.](sid-attributes-in-an-access-token.md)

In genere, il sistema usa il [*token di accesso*](/windows/desktop/SecGloss/p-gly) primario del thread che richiede l'accesso. Tuttavia, se il thread rappresenta un altro utente, il sistema utilizza il token di [*rappresentazione del thread.*](/windows/desktop/SecGloss/i-gly)

Il sistema esamina ogni ACE in sequenza fino a quando non si verifica uno degli eventi seguenti:

-   Una ACE con accesso negato nega in [](access-rights-and-access-masks.md) modo esplicito uno dei diritti di accesso richiesti a uno dei trustee elencati nel token di accesso del thread.
-   Uno o più ACE con accesso consentito per i trustee elencati nel token di accesso del thread concedono in modo esplicito tutti i diritti di accesso richiesti.
-   Tutte le voci ACE sono state controllate ed è ancora presente almeno un diritto di accesso richiesto che non è stato esplicitamente consentito. In questo caso, l'accesso viene negato in modo implicito.

Nella figura seguente viene illustrato come l'elenco DACL di un oggetto può consentire l'accesso a un thread negando l'accesso a un altro.

![dacl che concede diritti di accesso diversi a thread diversi](images/accctrl1.png)

Per il thread A, il sistema legge ACE 1 e nega immediatamente l'accesso perché la ACE per accesso negato si applica all'utente nel token di accesso del thread. In questo caso, il sistema non controlla le ACE 2 e 3. Per il thread B, ACE 1 non è applicabile, quindi il sistema passa ad ACE 2, che consente l'accesso in scrittura, e ACE 3, che consente l'accesso in lettura ed esecuzione.

Poiché il sistema smette di controllare le ACE quando l'accesso richiesto viene concesso o negato in modo esplicito, l'ordine delle ACE in un dacl è importante. Si noti che se l'ordine ACE è diverso nell'esempio, il sistema potrebbe aver concesso l'accesso al thread A. Per gli oggetti di sistema, il sistema operativo definisce un ordine [preferito di ACE in un dacl](order-of-aces-in-a-dacl.md).

 

 
