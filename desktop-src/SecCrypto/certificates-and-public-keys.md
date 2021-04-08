---
description: Servizi certificati è una base per l'infrastruttura a chiave pubblica (PKI) che fornisce i mezzi per la salvaguardia e l'autenticazione delle informazioni.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificati e chiavi pubbliche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e01993673fe16c8401368ffaa7e8815c450dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879982"
---
# <a name="certificates-and-public-keys"></a>Certificati e chiavi pubbliche

Servizi certificati è una base per l'infrastruttura a chiave pubblica (PKI) che fornisce i mezzi per la salvaguardia e l'autenticazione delle informazioni. La relazione tra un titolare del certificato, l'identità del proprietario del certificato e la [*chiave pubblica*](../secgloss/p-gly.md) del proprietario del certificato è una parte essenziale dell'infrastruttura PKI. Questa infrastruttura è costituita dalle parti seguenti:

-   [Coppia di chiavi pubblica/privata](#the-publicprivate-key-pair)
-   [Richiesta di certificato](#the-certificate-request)
-   [Autorità di certificazione](#the-certification-authority)
-   [Certificato](#the-certificate-request)
-   [Elenco di revoche di certificati](#the-certificate-revocation-list)
-   [Chiave pubblica usata per la crittografia](#your-public-key-used-for-encryption)
-   [Chiave pubblica usata per la verifica della firma](#your-public-key-used-for-signature-verification)
-   [Ruolo Servizi certificati Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Coppia di chiavi pubblica/privata

PKI richiede l'uso di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md). La matematica delle coppie di chiavi pubbliche/private esula dall'ambito di questa documentazione, ma è importante notare la relazione funzionale tra una chiave pubblica e una chiave privata. Gli [*algoritmi di crittografia*](../secgloss/c-gly.md) PKI utilizzano la [*chiave pubblica*](../secgloss/p-gly.md) del destinatario di un messaggio crittografato per crittografare i dati e la [*chiave privata*](../secgloss/p-gly.md) correlata e solo la chiave privata correlata per decrittografare il messaggio crittografato.

Analogamente, una [*firma digitale*](../secgloss/d-gly.md) del contenuto, descritta in dettaglio più avanti, viene creata con la chiave privata del firmatario. La chiave pubblica corrispondente, disponibile per tutti gli utenti, viene utilizzata per verificare la firma. La segretezza della chiave privata deve essere mantenuta perché il Framework si distingue dopo la compromissione della chiave privata.

Dato tempo e risorse sufficienti, una coppia di chiavi pubblica/privata può essere compromessa, ovvero la chiave privata può essere individuata. Più è lunga la chiave, più è difficile usare la forza bruta per individuare la chiave privata. In pratica, è possibile usare chiavi sufficientemente complesse per rendere impossibile determinare in modo tempestivo la chiave privata, rendendo l'infrastruttura a chiave pubblica un meccanismo di sicurezza valido.

Una chiave privata può essere archiviata in un disco in formato protetto, nel qual caso può essere usata solo con tale computer, a meno che non sia fisicamente spostata in un altro computer. Un'alternativa consiste nel disporre di una chiave su una smart card che può essere utilizzata in un computer diverso, purché disponga di un lettore di smart card e di un software di supporto.

La chiave pubblica, ma non la chiave privata, dell'oggetto di un certificato digitale è inclusa come parte della richiesta di [*certificato*](../secgloss/c-gly.md). (Pertanto, una coppia di chiavi pubblica/privata deve esistere prima di eseguire la richiesta di certificato). La chiave pubblica diventa parte del certificato emesso.

## <a name="the-certificate-request"></a>Richiesta di certificato

Prima di emettere un certificato, è necessario generare una [*richiesta di certificato*](../secgloss/c-gly.md) . Questa richiesta si applica a un'entità, ad esempio, un utente finale, un computer o un'applicazione. Per la discussione, si supponga che l'entità sia l'utente. I dettagli dell'identità sono inclusi nella richiesta di certificato. Una volta generata, la richiesta viene inviata a un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA). La CA USA quindi le informazioni di identità per determinare se la richiesta soddisfa i criteri della CA per il rilascio di un certificato. Se l'autorità di certificazione approva la richiesta, emette un certificato per l'utente, come l'entità denominata nella richiesta.

## <a name="the-certification-authority"></a>Autorità di certificazione

Prima di emettere il certificato, l'autorità di certificazione verifica l'identità. Quando il certificato viene emesso, l'identità viene associata al certificato, che contiene la chiave pubblica. Il certificato contiene anche la firma digitale dell'autorità di certificazione, che può essere verificata da chiunque riceva il certificato.

Poiché il certificato contiene l'identità della CA emittente, una parte interessata che considera attendibile l'autorità di certificazione può estendere tale trust al certificato. Il rilascio di un certificato non stabilisce una relazione di trust, ma trasferisce l'attendibilità. Se il consumer di certificati non considera attendibile la CA emittente, non sarà (o almeno non dovrebbe) considerare attendibile il certificato.

Una catena di certificati firmati consente il trasferimento dell'attendibilità anche ad altre CA. In questo modo, le entità che usano autorità di certificazione diverse possono comunque considerare attendibili i certificati (purché esista una CA comune nella catena, ovvero una CA considerata attendibile da entrambe le parti).

## <a name="the-certificate"></a>Certificato

Oltre alla chiave pubblica e all'identità della CA emittente, il certificato emesso contiene informazioni sugli scopi della chiave e del certificato. Include inoltre il percorso dell'elenco di certificati revocati della CA e specifica il periodo di validità del certificato (date di inizio e di fine).

Supponendo che il consumer di certificati consideri attendibile la CA emittente per il certificato, il consumer di certificati deve determinare se il certificato è ancora valido confrontando le date di inizio e fine del certificato con l'ora corrente e controllando che il certificato non sia presente nell'elenco dei certificati revocati della CA.

## <a name="the-certificate-revocation-list"></a>Elenco di revoche di certificati

Supponendo che il certificato venga usato in un periodo di tempo valido e che il consumer di certificati consideri attendibile la CA emittente, è disponibile un altro elemento che il consumer di certificati deve verificare prima di usare il certificato: l'elenco di revoche di [*certificati*](../secgloss/c-gly.md) (CRL). Il consumer di certificati controlla il CRL della CA (il percorso a cui è incluso come estensione nel certificato) per assicurarsi che il certificato non sia presente nell'elenco dei certificati revocati. I CRL sono disponibili perché talvolta un certificato non è scaduto, ma non può più essere considerato attendibile. Periodicamente, la CA pubblicherà un CRL aggiornato. I consumer di certificati sono responsabili del confronto dei certificati con l'elenco CRL corrente prima di considerare attendibile il certificato.

## <a name="your-public-key-used-for-encryption"></a>Chiave pubblica usata per la crittografia

Se un mittente vuole crittografare un messaggio prima di inviarlo all'utente, il mittente recupera prima il certificato. Dopo che il mittente ha determinato che la CA è attendibile e il certificato è valido e non è stato revocato, il mittente usa la chiave pubblica (ricordare che fa parte del certificato) con gli algoritmi di crittografia per crittografare il messaggio in [*testo*](../secgloss/p-gly.md) non crittografato in [*testo*](../secgloss/c-gly.md)crittografato. Quando si riceve il testo crittografato, si usa la chiave privata per decrittografare il testo crittografato.

Se una terza parte intercetta il messaggio di posta elettronica crittografato, la terza parte non sarà in grado di decrittografarla senza accedere alla [*chiave privata*](../secgloss/p-gly.md).

Si noti che la maggior parte delle attività elencate qui viene gestita dal software, non direttamente dall'utente.

## <a name="your-public-key-used-for-signature-verification"></a>Chiave pubblica usata per la verifica della firma

Una [*firma digitale*](../secgloss/d-gly.md) viene utilizzata per confermare che un messaggio non è stato modificato e come conferma dell'identità del mittente del messaggio. Questa firma digitale dipende dalla chiave privata e dal contenuto del messaggio. Utilizzando il messaggio come input e la chiave privata, gli algoritmi di crittografia creano la firma digitale. Il contenuto del messaggio non viene modificato dal processo di firma. Un destinatario può utilizzare la chiave pubblica (dopo aver verificato la validità del certificato, l'autorità di certificazione emittente e lo stato di revoca) per determinare se la firma corrisponde al contenuto del messaggio e per determinare se il messaggio è stato inviato dall'utente.

Se una terza parte intercetta il messaggio desiderato, lo modifica (anche leggermente) e lo trasmette e la firma originale al destinatario, il destinatario, all'esame del messaggio e della firma, sarà in grado di determinare che il messaggio è sospetto. Analogamente, se una terza parte crea un messaggio e lo invia con una firma digitale fasulla sotto il formato che ha originato da te, il destinatario potrà utilizzare la chiave pubblica per determinare che il messaggio e la firma non corrispondono tra loro.

Il non [*ripudio*](../secgloss/n-gly.md) è supportato anche dalle firme digitali. Se il mittente di un messaggio firmato nega l'invio del messaggio, il destinatario potrà utilizzare la firma per confutare tale attestazione.

Si noti che la maggior parte delle attività elencate qui viene gestita anche dal software, non direttamente dall'utente.

## <a name="microsoft-certificate-services-role"></a>Ruolo Servizi certificati Microsoft

Servizi certificati Microsoft ha il ruolo di emettere certificati o negare le richieste di certificati, come indicato dai moduli criteri, che hanno la responsabilità di garantire l'identità del richiedente del certificato. Servizi certificati offre inoltre la possibilità di revocare un certificato, nonché di pubblicare il CRL. I servizi certificati consentono inoltre di distribuire in modo centralizzato (ad esempio, a un servizio di directory) certificati emessi. La possibilità di emettere, distribuire, revocare e gestire certificati, insieme alla pubblicazione di CRL, fornisce le funzionalità necessarie per l'infrastruttura a chiave pubblica.

 

 
