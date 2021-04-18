---
description: I nomi di peer vengono utilizzati dal protocollo PNRP (Peer Name Resolution Protocol), da peer Identity Manager e dall'infrastruttura di raggruppamento peer.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Nomi di peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312240"
---
# <a name="peer-names"></a>Nomi di peer

I nomi di peer vengono utilizzati dal protocollo PNRP (Peer Name Resolution Protocol), da peer Identity Manager e dall'infrastruttura di raggruppamento peer. I nomi dei peer sono nomi stabili per le risorse, ad esempio computer, utenti, gruppi o servizi. PNRP usa i nomi dei peer per identificare i nodi in una rete peer.

> [!Note]  
> Un endpoint utilizzato dall'infrastruttura peer è in realtà una tupla costituita da un indirizzo IPv4 o IPv6, una porta e un protocollo (TCP o UDP). Un nome peer può avere più di una tupla.

 

Un nome peer è una stringa di testo con il formato seguente:

-   "Authority. Classificator"

Il valore di un'autorità varia a seconda che il nome sia protetto o non protetto. Il classificatore di un nome peer è una stringa. Un classificatore può essere un qualsiasi nome che contiene 150 o meno caratteri UNICODE. I nomi di peer fanno distinzione tra maiuscole e minuscole e possono essere registrati come protetti o non protetti. L'elenco seguente identifica alcuni esempi di nomi peer:

-   "0. MyUnsecuredPeerName"
-   "0. JohnDoe. Games"
-   "6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe

## <a name="secure-peer-names"></a>Nomi peer sicuri

Per un nome sicuro, l'autorità è l'hash SHA (Secure Hash Algorithm) della chiave pubblica del nome peer e restituisce una stringa esadecimale di 40 caratteri. Un nome peer sicuro può essere registrato solo con PNRP dal proprietario o dal delegato del proprietario del nome peer. È necessario creare un nome peer protetto chiamando [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).

## <a name="unsecured-peer-names"></a>Nomi peer non protetti

Per un nome non protetto, l'autorità è zero (0) e il classificatore è l'unica parte significativa del nome peer, che crea un nome peer non protetto senza un' [identità](identity-manager-api.md)associata. I nomi di peer non protetti vengono usati nella registrazione e nella risoluzione dei nomi PNRP. I nomi di peer non protetti forniscono un modo utile per registrare e risolvere le risorse che non richiedono la risoluzione dei nomi sicura. Qualsiasi nodo può tuttavia pubblicare qualsiasi nome non protetto. Le applicazioni interessate dalla sicurezza devono assicurarsi che siano solide e sicure nell'utilizzo di nomi di peer non protetti.

> [!Note]  
> Chiunque può registrare un nome peer non protetto con PNRP.

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP e l'istanza del nome peer più vicina

Può essere presente più di un'istanza di un nome peer. Quando si usa [PNRP](pnrp-namespace-provider-api.md) per risolvere un nome peer, esiste il concetto di un'istanza del nome peer **più vicina** , il che significa che il nome ha una posizione del servizio più vicina al membro di **sericat** specificato in [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) o [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)). Se non viene fornito alcun hint, più vicino a uno degli indirizzi IP locali.

 

 
