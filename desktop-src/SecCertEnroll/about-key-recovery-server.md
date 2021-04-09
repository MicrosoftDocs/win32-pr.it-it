---
description: È possibile configurare un'autorità di certificazione Microsoft (CA) per archiviare e ripristinare la chiave privata associata alla chiave pubblica inviata nella richiesta di certificato.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Server di ripristino chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9fd60b7ee6596b98953d382978be64695c035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881673"
---
# <a name="key-recovery-server"></a>Server di ripristino chiavi

È possibile configurare un'autorità di certificazione Microsoft (CA) per archiviare e ripristinare la chiave privata associata alla chiave pubblica inviata nella richiesta di certificato. Il ripristino è utile in caso di perdita di una chiave. Per impostazione predefinita, è possibile archiviare solo le chiavi di crittografia. Non è necessario archiviare le chiavi destinate solo alla firma perché è necessaria solo la chiave pubblica per verificare una firma se la chiave di firma privata viene persa.

Per archiviare una chiave, la CA deve essere configurata per emettere certificati di Key Recovery Agent (KRA) e per avere già emesso almeno uno. Un agente di recupero chiavi è un amministratore autorizzato da un'organizzazione a decrittografare le chiavi private. Per migliorare la sicurezza, è consigliabile assegnare l'agente di recupero chiavi e i ruoli di gestione certificati a singoli utenti, che il gestore di certificati sia autorizzato a recuperare ma non decrittografare le chiavi archiviate e che l'agente di recupero chiavi sia autorizzato a decrittografare le chiavi, ma non recuperarle.

## <a name="key-archival"></a>Archiviazione delle chiavi

Un client richiede in genere un certificato usando un modello. Se il modello richiede che la chiave privata venga archiviata, il client e la CA eseguono i passaggi seguenti:

1.  Il client recupera e convalida il certificato di scambio CA per determinare se è stato firmato con la stessa chiave usata per firmare il certificato di firma della CA. Ciò garantisce che l'unica autorità di certificazione in grado di decrittografare la chiave privata sia la CA da cui viene richiesto un certificato.
2.  La chiave pubblica nel certificato di scambio CA viene usata per crittografare la chiave privata associata alla richiesta di certificato e la richiesta viene inviata all'autorità di certificazione.
3.  La CA USA la chiave privata associata al certificato di Exchange per decrittografare la chiave privata inviata dal client e verifica che le chiavi pubbliche e private nella richiesta siano correlate.
4.  La CA crittografa la chiave privata utilizzando la chiave pubblica nel certificato KRA. Se la CA ha emesso più certificati KRA, crittografa la chiave privata una volta con ogni chiave pubblica disponibile, in modo che qualsiasi agente di recupero chiavi autorizzato possa recuperare una chiave. Le chiavi private crittografate vengono archiviate nel database dei certificati.
5.  La CA rilascia tutti i riferimenti alla chiave privata e libera in modo sicuro e azzera tutta la memoria che contiene la chiave. In questo modo, l'autorità di certificazione non ha più accesso alla chiave in formato testo non crittografato.

> [!Note]  
> Solo una richiesta CMC può essere usata per l'archiviazione delle chiavi. Le richieste CMC sono rappresentate dall'interfaccia [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

 

## <a name="key-recovery"></a>Recupero chiavi

Il recupero delle chiavi non è supportato direttamente da Servizi certificati Active Directory o dall'API di registrazione certificati. Microsoft, tuttavia, fornisce le seguenti applicazioni per semplificare il processo:

-   Certutil.exe è un programma da riga di comando che può essere usato per recuperare le informazioni di configurazione della CA, verificare i certificati, le coppie di chiavi e le catene di certificati, nonché eseguire il backup e il ripristino delle chiavi. È incluso nei sistemi operativi server a partire da Windows Server 2003.
-   Krecover.exe è un programma basato su finestra di dialogo che consente il recupero della chiave. È incluso nel Resource Kit a partire da Windows Server 2003.

Per recuperare una chiave privata vengono eseguiti i passaggi seguenti:

1.  Il gestore di certificati individua potenziali candidati per il ripristino della chiave nel database del certificato usando il nome del certificato, del richiedente o dell'utente. A questo scopo, è possibile usare il comando **certutil** **-GetKey** .
2.  Una volta che il gestore di certificati dispone di un elenco di certificati, il comando **-GetKey** viene richiamato con un numero di serie del certificato specifico o una stampa Thumb per recuperare un \# file PKCS 7 che contiene il certificato Kra, la catena di certificati utente e la chiave privata crittografata durante l'archiviazione tramite la chiave pubblica Kra.
3.  Il gestore di certificati passa il controllo del processo all'agente di recupero chiavi la cui chiave privata corrisponde alla chiave pubblica contenuta nel certificato KRA.
4.  L'agente di recupero chiavi decrittografa la chiave privata archiviata restituita nel \# file PKCS 7 utilizzando la chiave privata Kra. Questa operazione può essere eseguita usando il comando **certutil** **-recoverkey** che inserisce la chiave in un file PKCS 12 protetto da password \# . Al client deve essere assegnata la password tramite un meccanismo fuori banda sicuro.
5.  Il client importa il \# file PKCS 12 e usa la password per recuperare la chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 



