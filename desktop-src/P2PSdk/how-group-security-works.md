---
description: Per i gruppi peer è necessario che ogni membro disponga di un certificato specifico, denominato gruppo di certificati del membro del gruppo (GMC).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Funzionamento della sicurezza del gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881798"
---
# <a name="how-group-security-works"></a>Funzionamento della sicurezza del gruppo

Per i gruppi peer è necessario che ogni membro disponga di un certificato specifico, denominato gruppo di certificati del membro del gruppo (GMC). Il certificato GMC garantisce che tutti i record scambiati tra i peer siano firmati digitalmente. La chiave pubblica di un peer è contenuta nelle strutture passate come parte della comunicazione tra peer, incluse le [**\_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).

È possibile emettere un GMC in una catena. Un autore può ad esempio emettere un GMC per l'amministratore A, che può emettere un GMC all'amministratore B, che può emettere un GMC al membro M. La catena di GMC risultante è: Creator->A->B->M, che ha una lunghezza pari a 4. La lunghezza della catena è importante, perché non può essere maggiore di 24. Se il 24 ° amministratore di una catena tenta di emettere una GMC per un membro, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) o [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) restituisce una catena di peer \_ E \_ \_ troppo \_ lungo.

È anche possibile emettere un GMC chiamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Un GMC implica l'appartenenza dell'utente al gruppo per cui è stato emesso il GMC e può avere una durata finita o infinita. L'attività membro del gruppo non può essere più lunga della durata specificata in GMC.

> [!Note]  
> La durata della GMC infinita è attualmente impostata su 1000 anni.

 

L'attività membro del gruppo è limitata dalla durata di GMC e include quanto segue:

-   **Operazioni di registrazione** : un peer non è in grado di pubblicare informazioni in un gruppo dopo la scadenza dell'appartenenza al gruppo o di pubblicare record con una durata superiore alla durata dell'appartenenza al gruppo del peer.
-   **Operazioni di appartenenza** : un amministratore di gruppo non può emettere un'appartenenza con una durata superiore alla data specificata nell'appartenenza dell'amministratore del gruppo. Se, ad esempio, un amministratore ha 500 ore rimanenti per la durata di GMC, tutte le appartenenze emesse devono essere inferiori a 500 ore.

Poiché un membro del gruppo non può avere una durata superiore a quella dell'amministratore che invita il membro del gruppo, è consigliabile impostare la durata di GMC di un amministratore come infinita o per una durata molto lunga. Per impostazione predefinita, l'autore del gruppo ha una durata infinita.

## <a name="renewing-group-membership"></a>Rinnovo dell'appartenenza al gruppo

Per rinnovare le credenziali di un amministratore o di un membro la cui durata di GMC è pronta per scadere, sono disponibili le due opzioni seguenti:

-   Chiamare [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) e passare l'identità del membro la cui durata è pronta per scadere. Se le credenziali vengono specificate come **null** e le informazioni sull'appartenenza del peer sono disponibili per il gruppo, il tempo di rinnovo viene impostato sulla stessa durata specificata nelle credenziali membro pubblicate in precedenza. Se è necessario specificare un periodo di durata diverso, è necessario fornire una nuova struttura di [**\_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) che contenga la nuova durata della durata, quindi viene pubblicata una nuova GMC per il membro.

    La funzione [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) accetta facoltativamente il \_ flag di credenziali dell'archivio del gruppo peer \_ \_ , che pubblica automaticamente le nuove credenziali del membro nel database del gruppo. Quando il membro si connette al gruppo la volta successiva, per la prima volta o dopo il passaggio offline, il membro ottiene il GMC aggiornato dal database.

-   Chiamare [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) per passare l'identità del membro la cui durata di GMC è pronta per scadere. Se la scadenza specificata nell'invito è **null**, il periodo di validità della GMC è uguale a quello dell'amministratore GMC che rilascia l'appartenenza. Se il creatore specifica la scadenza come **null**, viene emesso un GMC con una durata infinita.

    Se un peer viene emesso un GMC che scade prima del valore della durata della presenza, gli indirizzi del peer non sono disponibili nelle strutture [**del \_ membro peer**](/windows/desktop/api/P2P/ns-p2p-peer_member) restituite nell'enumerazione iniziata da una chiamata a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Questo problema si verifica perché le informazioni sulla presenza non vengono pubblicate in questo caso, anche se il flag di presenza del PEER \_ Disable \_ non è impostato.

 

 



