---
description: In questo argomento viene illustrato il processo di invito di un peer a partecipare a un gruppo peer mediante le API di raggruppamento peer.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Invito di un peer a un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b1e8852f58387d424944d4a8821f56b5e11e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967536"
---
# <a name="inviting-a-peer-to-a-group"></a>Invito di un peer a un gruppo

In questo argomento viene illustrato il processo di invito di un peer a partecipare a un gruppo peer mediante le API di raggruppamento peer.

Un gruppo peer richiede credenziali valide per partecipare. Le credenziali vengono emesse dall'esterno di un gruppo sotto forma di inviti o direttamente ai membri all'interno di un gruppo quando sono necessari aggiornamenti delle credenziali.

## <a name="group-member-certificates"></a>Certificati dei membri del gruppo

Un gruppo peer viene creato quando un'applicazione effettua una chiamata a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).

Per partecipare a un gruppo peer, ogni peer deve avere un'identità peer. Chiamare [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) fino a quando non vengono restituite tutte le identità peer definite per il peer e selezionare quella da usare. Se non esiste un'identità peer, crearne una chiamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Ogni identità peer è associata a un set di credenziali specifico che può essere usato per dimostrare l'appartenenza al gruppo peer durante la connessione, nonché per la pubblicazione di record o l'invito di altri membri. Queste credenziali sono rappresentate come catene di [certificati X. 509](https://www.ietf.org/rfc/rfc2511.txt) denominati certificati di appartenenza a gruppi (GMC).

Per creare il GMC per un'identità peer, è necessario prima ottenere la relativa chiave pubblica. Questa chiave viene ottenuta chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sul potenziale invito e passando la relativa identità peer. Questa funzione restituisce un certificato con codifica base 64 (IDC) che contiene la chiave pubblica RSA usata per creare la GMC per l'identità peer (tra le altre cose), incapsulata in un BLOB XML, nel formato seguente:

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Questa stringa può essere passata a [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), che restituisce un invito che contiene il GMC per l'identità peer. L'invito deve essere passato all'invito usando un processo diverso, ad esempio posta elettronica, FTP o una condivisione file sicura.

In alternativa, l'IDC stesso può essere inserito in una nuova struttura di [**\_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) e passata a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials), che genera un invito.

Si noti che le applicazioni non possono aggiungere tag all'interno del tag **PEERIDENTITYINFO** o modificare in alcun modo il frammento XML. Le applicazioni possono incorporare questo frammento XML in altri documenti XML, ma devono rimuovere tutti i file XML specifici dell'applicazione prima di passare questo frammento alle funzioni [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) .

I membri GMCs vengono emessi dagli amministratori e dall'autore del gruppo peer. I membri devono ottenere nuovi GMCs con durate estese il GMCs prima che venga superata l'ora di scadenza. L'amministratore del gruppo peer rilascia le credenziali aggiornate chiamando [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) con le credenziali esistenti per tale peer.

La struttura di [**\_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contiene i dati di base sullo stato di appartenenza di un peer, inclusa la chiave pubblica per la relativa GMC. Le credenziali appena rilasciate possono essere pubblicate nel gruppo peer impostando il \_ flag delle credenziali dell'archivio del gruppo peer \_ \_ nella chiamata a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Quando il destinatario delle nuove credenziali viene aggiunto al gruppo peer, le credenziali esistenti verranno aggiornate dall'infrastruttura di raggruppamento dei peer.

## <a name="issuing-an-invitation"></a>Invio di un invito

Un membro viene invitato a partecipare al gruppo peer in uno dei due modi seguenti:

-   Un amministratore del gruppo peer chiama [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), passando la stringa XML delle informazioni di identità ottenuta dal potenziale invito tramite un meccanismo fuori banda comune, ad esempio un messaggio di posta elettronica o una sessione di messaggistica immediata. L'invito viene inoltre passato attraverso un processo o un meccanismo esterno al peer, che lo riceverà come una stringa XML o un file di testo.
-   Un amministratore del gruppo peer chiama [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Per usare questa funzione, il peer deve avere già pubblicato le informazioni di appartenenza al gruppo peer [**( \_ membro peer**](/windows/desktop/api/P2P/ns-p2p-peer_member)) o avere una chiave pubblica disponibile (della coppia di chiavi RSA usata per creare l'identità del soggetto). Nel primo caso, la struttura [**delle \_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) necessaria per **PeerGroupIssueCredentials** può essere ottenuta dalla struttura del **\_ membro peer** . nel secondo caso, una nuova struttura di **\_ \_ informazioni sulle credenziali peer** può essere popolata con la chiave pubblica.

Dopo aver ricevuto la stringa di invito, il peer lo passa a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) per l'aggiunta al gruppo peer. Se la chiamata a **PeerGroupJoin** ha esito positivo, il peer può aprire successivamente il gruppo peer chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Analisi di un invito

Facoltativamente, è possibile analizzare un invito chiamando [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), che restituisce una struttura di [**\_ \_ informazioni di invito peer**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) . I campi della struttura possono essere facilmente ottenuti a scopo di visualizzazione.

 

 



