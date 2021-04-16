---
description: Quando un thread tenta di accedere a un oggetto a protezione diretta, il sistema concede o nega l'accesso.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Funzionamento di AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563796"
---
# <a name="how-accesscheck-works"></a>Funzionamento di AccessCheck

Quando un thread tenta di accedere a un oggetto a protezione diretta, il sistema concede o nega l'accesso. Se l'oggetto non dispone di un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL), il sistema concede l'accesso; in caso contrario, il sistema cerca le [voci di controllo di accesso](access-control-entries.md) (ACE) nell'elenco DACL dell'oggetto che si applicano al thread. Ogni voce ACE nel DACL dell'oggetto specifica i diritti di accesso consentiti o negati per un [trustee](trustees.md), che può essere un account utente, un account di gruppo o una [*sessione di accesso*](/windows/desktop/SecGloss/l-gly).

## <a name="dacls"></a>DACL

Il sistema confronta il trustee in ogni voce ACE con i trustee identificati nel token di [accesso](access-tokens.md)del thread. Un token di accesso contiene gli [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che identificano l'utente e gli account di gruppo a cui appartiene l'utente. Un token contiene anche un [*SID di accesso*](/windows/desktop/SecGloss/l-gly) che identifica la sessione di accesso corrente. Durante un controllo di accesso, il sistema ignora i SID di gruppo che non sono abilitati. Per ulteriori informazioni sui SID abilitati, disabilitati e di sola negazione, vedere [attributi SID in un token di accesso](sid-attributes-in-an-access-token.md).

In genere, il sistema usa il [*token di accesso primario*](/windows/desktop/SecGloss/p-gly) del thread che richiede l'accesso. Tuttavia, se il thread rappresenta un altro utente, il sistema usa il [*token di rappresentazione*](/windows/desktop/SecGloss/i-gly)del thread.

Il sistema esamina ogni voce ACE in sequenza fino a quando non si verifica uno degli eventi seguenti:

-   Una voce ACE con accesso negato nega in modo esplicito i [diritti di accesso](access-rights-and-access-masks.md) richiesti a uno dei trustee elencati nel token di accesso del thread.
-   Una o più voci ACE consentite per l'accesso per i trustee elencate nel token di accesso del thread concedono in modo esplicito tutti i diritti di accesso richiesti.
-   Tutte le voci ACE sono state controllate ed è ancora presente almeno un diritto di accesso richiesto che non è stato esplicitamente consentito. in questo caso, l'accesso viene negato in modo implicito.

Nella figura seguente viene illustrato il modo in cui un DACL dell'oggetto può consentire l'accesso a un thread negando l'accesso a un altro thread.

![DACL che concede diritti di accesso diversi a thread diversi](images/accctrl1.png)

Per il thread A, il sistema legge ACE 1 e nega immediatamente l'accesso perché la voce ACE di accesso negato si applica all'utente nel token di accesso del thread. In questo caso, il sistema non controlla le voci ACE 2 e 3. Per il thread B, ACE 1 non è applicabile, quindi il sistema passa a ACE 2, che consente l'accesso in scrittura e ACE 3, che consente l'accesso in lettura ed esecuzione.

Poiché il sistema interrompe il controllo degli ACE quando l'accesso richiesto viene concesso o negato in modo esplicito, l'ordine delle voci ACE in un DACL è importante. Si noti che se l'ordine ACE è diverso nell'esempio, il sistema potrebbe avere concesso l'accesso al thread A. Per gli oggetti di sistema, il sistema operativo definisce un ordine preferenziale [di voci ACE in un DACL](order-of-aces-in-a-dacl.md).

 

 
