---
description: Un'autorità di certificazione (CA) Microsoft può essere configurata per archiviare e ripristinare la chiave privata associata alla chiave pubblica inviata nella richiesta di certificato.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Server di ripristino chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903774"
---
# <a name="key-recovery-server"></a>Server di ripristino chiavi

Un'autorità di certificazione (CA) Microsoft può essere configurata per archiviare e ripristinare la chiave privata associata alla chiave pubblica inviata nella richiesta di certificato. Il ripristino è utile in caso di perdita di una chiave. Per impostazione predefinita, è possibile archiviare solo le chiavi di crittografia. Non è necessario archiviare le chiavi destinate solo alla firma perché è necessaria solo la chiave pubblica per verificare una firma in caso di perdita della chiave di firma privata.

Per archiviare una chiave, l'autorità di certificazione deve essere configurata per rilasciare certificati dell'agente di recupero chiavi e per aver già emesso almeno uno. Un agente di recupero chiavi è un amministratore autorizzato da un'organizzazione a decrittografare le chiavi private. Per migliorare la sicurezza, è consigliabile assegnare l'agente di recupero chiavi e i ruoli di gestione certificati a utenti diversi, che il gestore di certificati sia autorizzato a recuperare ma non decrittografare le chiavi archiviate e che l'agente di recupero chiavi sia autorizzato a decrittografare le chiavi, ma non a recuperarle.

## <a name="key-archival"></a>Archivio chiavi

Un client richiede in genere un certificato usando un modello. Se il modello richiede l'archiviazione della chiave privata, il client e l'autorità di certificazione eseguiti dai passaggi seguenti:

1.  Il client recupera e convalida il certificato di scambio ca per determinare se è stato firmato dalla stessa chiave usata per firmare il certificato di firma della CA. Ciò garantisce che l'unica AUTORITÀ di certificazione in grado di decrittografare la chiave privata sia la CA da cui viene richiesto un certificato.
2.  La chiave pubblica nel certificato di scambio della CA viene usata per crittografare la chiave privata associata alla richiesta di certificato e la richiesta viene inviata alla CA.
3.  La CA usa la chiave privata associata al certificato di scambio per decrittografare la chiave privata inviata dal client e verifica che le chiavi pubbliche e private nella richiesta siano correlate.
4.  L'autorità di certificazione crittografa la chiave privata usando la chiave pubblica nel certificato DELL'autorità di certificazione. Se l'autorità di certificazione ha emesso più certificati DELLA CA, crittografa la chiave privata una sola volta con ogni chiave pubblica disponibile in modo che qualsiasi agente di recupero chiavi autorizzato possa recuperare una chiave. Le chiavi private crittografate vengono archiviate nel database dei certificati.
5.  L'autorità di certificazione rilascia tutti i riferimenti alla chiave privata e libera e azzera in modo sicuro tutta la memoria che contiene la chiave. Ciò garantisce che l'autorità di certificazione non abbia accesso alla chiave in formato testo non crittografato.

> [!Note]  
> Solo una richiesta CMC può essere usata per l'archiviazione delle chiavi. Le richieste CMC sono rappresentate [**dall'interfaccia IX509CertificateRequestCmc.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)

 

## <a name="key-recovery"></a>Recupero chiavi

Il ripristino delle chiavi non è supportato direttamente da Servizi certificati Active Directory o dall'API di registrazione certificati. Microsoft fornisce tuttavia le applicazioni seguenti per facilitare il processo:

-   Certutil.exe è un programma da riga di comando che può essere usato per recuperare le informazioni di configurazione della CA, verificare certificati, coppie di chiavi e catene di certificati ed eseguire il backup e il ripristino delle chiavi. È incluso nei sistemi operativi server a partire da Windows Server 2003.
-   Krecover.exe è un programma basato su finestre di dialogo che consente il ripristino delle chiavi. È incluso nel Resource Kit a partire da Windows Server 2003.

Per ripristinare una chiave privata, vengono eseguiti i passaggi seguenti:

1.  Il gestore di certificati individua i potenziali candidati per il ripristino delle chiavi nel database dei certificati usando il nome del certificato, del richiedente o dell'utente. A questo scopo, è possibile usare il comando **Certutil** **-getkey.**
2.  Dopo che il gestore di certificati ha un elenco di certificati, il **comando -getkey** viene chiamato nuovamente con un numero di serie del certificato specifico o una stampa thumb per recuperare un file PKCS 7 che contiene il certificato PKCS, la catena di certificati utente e la chiave privata crittografata durante l'archiviazione usando la chiave pubblica \# PKCS 7.
3.  Il gestore di certificati passa il controllo del processo all'agente di recupero chiavi la cui chiave privata corrisponde alla chiave pubblica contenuta nel certificato CERTIFICAZIONE.
4.  L'agente di recupero chiavi decrittografa la chiave privata archiviata restituita nel file PKCS \# 7 usando la chiave privata PKCS 7. Questa operazione può essere eseguita usando il **comando Certutil** **-recoverkey** che inserisce la chiave in un file PKCS \# 12 protetto da password. Al client deve essere data la password tramite un meccanismo fuori banda sicuro.
5.  Il client importa il file PKCS \# 12 e usa la password per recuperare la chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 



