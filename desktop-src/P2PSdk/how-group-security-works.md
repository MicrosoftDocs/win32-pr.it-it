---
description: I gruppi peer richiedono che ogni membro abbia un certificato specifico, denominato certificato membro del gruppo( GMC).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Funzionamento della sicurezza dei gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941b4bded19b914218d5c011e8696cdd9c92612a493954dc5dd45d91e59006a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675211"
---
# <a name="how-group-security-works"></a>Funzionamento della sicurezza dei gruppi

I gruppi peer richiedono che ogni membro abbia un certificato specifico, denominato certificato membro del gruppo( GMC). Il certificato GMC garantisce che tutti i record s scambiati tra peer siano firmati digitalmente. La chiave pubblica di un peer è contenuta nelle strutture passate come parte della comunicazione tra peer, tra cui [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).

Un GMC può essere rilasciato in una catena. Ad esempio, un creatore può rilasciare un GMC all'amministratore A, che può rilasciare un GMC all'amministratore B, che può rilasciare un GMC al membro M. La catena GMC risultante è: creator->A->B->M, che ha una lunghezza di 4. La lunghezza della catena è importante perché non può essere più lunga di 24. Se il 24° amministratore di una catena tenta di rilasciare un GMC a un membro, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) o [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) restituisce PEER \_ E CHAIN TOO \_ \_ \_ LONG.

Un GMC può essere emesso anche chiamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Un GMC implica l'appartenenza dell'utente al gruppo per cui viene rilasciata la console GMC e può avere una durata finita o infinita. L'attività del membro del gruppo non può essere più lunga della durata specificata in GMC.

> [!Note]  
> La durata infinita di GMC è attualmente impostata su 1000 anni.

 

L'attività dei membri del gruppo è limitata dalla durata di GMC e include quanto segue:

-   **Operazioni sui** record: un peer non può pubblicare informazioni in un gruppo dopo la scadenza dell'appartenenza al gruppo o pubblicare record con una durata superiore alla durata dell'appartenenza al gruppo del peer.
-   **Operazioni di appartenenza:** un amministratore di gruppo non può rilasciare un'appartenenza con una durata successiva alla data specificata nell'appartenenza dell'amministratore di gruppo. Ad esempio, se un amministratore ha 500 ore rimanenti per la durata di GMC, tutte le appartenenze rilasciate devono essere inferiori a 500 ore.

Poiché un membro del gruppo non può avere una durata superiore a quella dell'amministratore che lo invita, è consigliabile impostare la durata GMC di un amministratore come infinita o per una durata molto lunga. Per impostazione predefinita, l'autore del gruppo ha una durata infinita.

## <a name="renewing-group-membership"></a>Rinnovo dell'appartenenza a gruppi

Per rinnovare le credenziali di un amministratore o di un membro la cui durata GMC è pronta per scadere, sono disponibili le due opzioni seguenti:

-   Chiamare [**PeerGroupIssueCredentials e**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) passare l'identità del membro la cui durata è pronta per scadere. Se le credenziali vengono specificate come **NULL** e le informazioni di appartenenza del peer sono disponibili per il gruppo, l'ora di rinnovo viene impostata sulla stessa durata specificata nelle credenziali del membro pubblicate in precedenza. Se è necessario specificare un periodo di durata diverso, è necessario specificare una nuova struttura [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) che contenga la nuova durata e quindi viene pubblicata una nuova console di gestione delle chiavi per il membro.

    La [**funzione PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) accetta facoltativamente il flag PEER \_ GROUP STORE \_ CREDENTIALS, che pubblica automaticamente le nuove credenziali del membro nel \_ database del gruppo. Quando il membro si connette al gruppo la volta successiva, per la prima volta o dopo la modalità offline, il membro ottiene il GMC aggiornato dal database.

-   Chiamare [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) per passare l'identità del membro la cui durata GMC è pronta per scadere. Se la scadenza specificata nell'invito è **NULL,** la durata del GMC è la stessa dell'amministratore GMC che invia l'appartenenza. Se l'autore specifica la scadenza come **NULL,** viene emesso un GMC con una durata infinita.

    Se a un peer viene emesso un GMC che scade prima del valore di durata della presenza, gli indirizzi del peer non sono disponibili nelle strutture [**PEER \_ MEMBER**](/windows/desktop/api/P2P/ns-p2p-peer_member) restituite nell'enumerazione avviata da una chiamata a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Ciò si verifica perché le informazioni sulla presenza non vengono pubblicate in questo caso, anche se il \_ flag PEER DISABLE PRESENCE non è \_ impostato.

 

 



