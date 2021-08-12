---
description: Questo argomento illustra il processo di invito di un peer a partecipare a un gruppo peer usando le API di raggruppamento peer.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Invito di un peer a un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760c2fb6023d5332da74402726669367fee4f5102c99269fa8e603653a1e2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612651"
---
# <a name="inviting-a-peer-to-a-group"></a>Invito di un peer a un gruppo

Questo argomento illustra il processo di invito di un peer a partecipare a un gruppo peer usando le API di raggruppamento peer.

Un gruppo peer richiede credenziali valide per partecipare. Le credenziali vengono rilasciate dall'esterno di un gruppo sotto forma di inviti o direttamente ai membri all'interno di un gruppo quando sono necessari aggiornamenti delle credenziali.

## <a name="group-member-certificates"></a>Certificati dei membri del gruppo

Un gruppo peer viene creato quando un'applicazione esegue una chiamata a [**PeerGroupCreate.**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)

Per partecipare a un gruppo peer, ogni peer deve avere un'identità peer. Chiamare [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) finché non vengono restituite tutte le identità peer definite per il peer e selezionare quella da usare. Se non esiste un'identità peer, crearne una chiamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Ogni identità peer è associata a un set specifico di credenziali che possono essere usate per dimostrare l'appartenenza al gruppo peer durante la connessione, nonché quando si pubblicano record o si invitano membri aggiuntivi. Queste credenziali sono rappresentate come catene di [certificati X.509](https://www.ietf.org/rfc/rfc2511.txt) denominati certificati di appartenenza a gruppi (GMC).

Per creare GMC per un'identità peer, è prima necessario ottenerne la chiave pubblica. Questa chiave viene ottenuta chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sul potenziale invitato e passando la relativa identità peer. Questa funzione restituisce un certificato con codifica base 64 (IDC) che contiene la chiave pubblica RSA usata per creare la GMC per l'identità peer (tra le altre cose), incapsulata in un BLOB XML, nel formato seguente:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Questa stringa può essere passata a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), che restituisce un invito che contiene il GMC per l'identità del peer. L'invito deve essere passato all'invitato usando un processo diverso, ad esempio posta elettronica, FTP o una condivisione file sicura.

In alternativa, L'IDC stesso può essere inserito in una nuova struttura [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) e passato a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials), che genera allo stesso modo un invito.

Si noti che alle applicazioni non è consentito aggiungere tag all'interno del tag **PEERIDENTITYINFO** o modificare questo frammento XML in alcun modo. Le applicazioni possono incorporare questo frammento XML in altri documenti XML, ma devono rimuovere tutto il codice XML specifico dell'applicazione prima di passare questo frammento alle funzioni [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) [**o PeerGroupIssueCredentials.**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)

I gmc membri vengono emessi dagli amministratori e dall'autore del gruppo peer. I membri devono ottenere nuovi GMC con durate estese prima che sia trascorsa l'ora di scadenza. L'amministratore del gruppo peer emette le credenziali aggiornate chiamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) con le credenziali esistenti per tale peer.

La [**struttura PEER CREDENTIAL \_ \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contiene i dati di base sullo stato di appartenenza di un peer, inclusa la chiave pubblica per GMC. Le credenziali appena rilasciate possono essere pubblicate nel gruppo peer impostando il flag PEER GROUP STORE CREDENTIALS nella chiamata \_ \_ a \_ [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Quando il destinatario delle nuove credenziali si aggiunge al gruppo peer, le credenziali esistenti verranno aggiornate dall'infrastruttura di raggruppamento peer.

## <a name="issuing-an-invitation"></a>Emissione di un invito

Un membro viene invitato a partecipare al gruppo peer in uno dei due modi seguenti:

-   Un amministratore del gruppo peer chiama [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), passando la stringa XML delle informazioni sull'identità ottenuta dal potenziale invitato tramite un meccanismo fuori banda comune, ad esempio la posta elettronica o una sessione di messaggistica immediata. L'invito viene anche passato tramite un processo o un meccanismo esterno al peer, che alla fine lo riceverà come stringa XML o file di testo.
-   Un amministratore del gruppo peer chiama [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Per usare questa funzione, il peer deve avere già pubblicato le informazioni sull'appartenenza al gruppo peer ([**PEER \_ MEMBER**](/windows/desktop/api/P2P/ns-p2p-peer_member)) o avere una chiave pubblica disponibile (della coppia di chiavi RSA usata per creare l'identità del soggetto). Nel primo caso, la struttura PEER CREDENTIAL INFO necessaria per **PeerGroupIssueCredentials** può essere ottenuta dalla struttura **PEER \_ MEMBER.** Nel secondo caso, una nuova struttura **PEER CREDENTIAL \_ \_** [**\_ \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) può essere popolata con la chiave pubblica.

Dopo aver ricevuto la stringa di invito, il peer la passa a [**PeerGroupJoin per**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) unirsi al gruppo peer. Se la chiamata a **PeerGroupJoin** ha esito positivo, il peer può successivamente aprire il gruppo peer chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Analisi di un invito

Facoltativamente, un invito può essere analizzato chiamando [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), che restituisce una [**struttura PEER INVITATION \_ \_ INFO.**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) I campi nella struttura possono essere facilmente ottenuti a scopo di visualizzazione.

 

 



