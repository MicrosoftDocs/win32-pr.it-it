---
title: Binding con crittografia
description: I dati sensibili scambiati in una rete devono essere crittografati.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associazione con crittografia
- Binding con crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955110"
---
# <a name="binding-with-encryption"></a>Binding con crittografia

I dati sensibili scambiati in una rete devono essere crittografati. Per consentire questa operazione, ADSI supporta due tipi di crittografia, Kerberos e Secure Sockets Layer (SSL). Entrambi i tipi di crittografia richiedono l'uso di [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per l'associazione.

Non è possibile utilizzare **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per l'associazione in questo caso perché queste funzioni causano le richieste LDAP utilizzate da ADSI e i dati restituiti dal server di directory per la trasmissione in rete come testo non crittografato. Ai fini del debug, è utile disattivare la crittografia in modo che sia possibile usare la Network Monitor per visualizzare le richieste e i dati LDAP tra il client e il server di directory.

## <a name="kerberos-based-encryption"></a>Crittografia basata su Kerberos

Per usare la crittografia basata su Kerberos, specificare il flag di **\_ \_ sealing use di ADS** quando si chiama [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Per verificare l'integrità dei dati è anche possibile usare il flag di **\_ \_ sealing use ADS** , ovvero per assicurarsi che i dati ricevuti corrispondano ai dati inviati. Se viene specificato il flag di **\_ \_ sealing use** , viene specificato automaticamente anche il flag di **\_ \_ firma use** . Entrambi i flag richiedono l'autenticazione Kerberos, che funziona solo nelle condizioni seguenti:

-   Il computer client deve essere connesso al dominio di Windows o a un dominio considerato attendibile da un dominio di Windows.
-   [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) deve essere chiamato con credenziali null; ovvero non è possibile specificare credenziali alternative.

## <a name="ssl-based-encryption"></a>Crittografia basata su SSL

Per usare la crittografia basata su SSL, specificare gli **annunci usare il flag \_ \_ SSL** quando si chiama [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Se viene specificato solo l'opzione **Ads \_ use \_ SSL** flag, ADSI apre la porta SSL 636 e quindi esegue un'associazione semplice sul canale SSL. Se vengono specificati sia l' **\_ \_ autenticazione protetta** ADS che gli annunci, il comportamento dell'associazione dipende dal client da cui viene effettuata la chiamata. **\_ \_** Nelle versioni di Windows non supportate, ADSI ha aperto prima di tutto un canale SSL ed esegue un'associazione semplice usando il nome utente e la password specificati oppure il contesto utente corrente se il nome utente e la password sono null. Nelle versioni supportate di Windows, ADSI esegue un'autenticazione protetta anziché un'associazione semplice.

Per usare la crittografia basata su SSL durante la comunicazione con Active Directory, Active Directory necessario avere abilitato l'infrastruttura a chiave pubblica (PKI). L'infrastruttura a chiave pubblica può essere abilitata impostando un'autorità di certificazione dell'organizzazione (Enterprise) in uno dei server in Active Directory, inclusa una delle Active Directory Server. La configurazione di un'autorità di certificazione globale (Enterprise) fa sì che un server di Active Directory ottenga un certificato del server che può essere usato per eseguire la crittografia basata su SSL.

 

 




