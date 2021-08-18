---
description: Servizi certificati è una delle basi per l'infrastruttura a chiave pubblica (PKI) che fornisce i mezzi per la protezione e l'autenticazione delle informazioni.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificati e chiavi pubbliche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d5f1996549184b8c56388bdb3ae8395eee077bca31b03e074f4dda8568805b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770621"
---
# <a name="certificates-and-public-keys"></a>Certificati e chiavi pubbliche

Servizi certificati è una delle basi per l'infrastruttura a chiave pubblica (PKI) che fornisce i mezzi per la protezione e l'autenticazione delle informazioni. La relazione tra il titolare di un certificato, l'identità del titolare del certificato e la chiave pubblica del titolare del certificato [*è*](../secgloss/p-gly.md) una parte critica dell'infrastruttura a chiave pubblica. Questa infrastruttura è costituito da parti seguenti:

-   [Coppia di chiavi pubblica/privata](#the-publicprivate-key-pair)
-   [Richiesta di certificato](#the-certificate-request)
-   [Autorità di certificazione](#the-certification-authority)
-   [Certificato](#the-certificate-request)
-   [Elenco di revoche di certificati](#the-certificate-revocation-list)
-   [Chiave pubblica usata per la crittografia](#your-public-key-used-for-encryption)
-   [Chiave pubblica usata per la verifica della firma](#your-public-key-used-for-signature-verification)
-   [Ruolo di Servizi certificati Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Coppia di chiavi pubblica/privata

L'infrastruttura a chiave pubblica richiede [*l'uso di coppie di chiavi pubbliche/private.*](../secgloss/p-gly.md) La matematica delle coppie di chiavi pubbliche/private non è compresa nell'ambito di questa documentazione, ma è importante notare la relazione funzionale tra una chiave pubblica e una chiave privata. Gli algoritmi [*di*](../secgloss/c-gly.md) crittografia [](../secgloss/p-gly.md) PKI usano la chiave pubblica del destinatario di [](../secgloss/p-gly.md) un messaggio crittografato per crittografare i dati e la chiave privata correlata e solo la chiave privata correlata per decrittografare il messaggio crittografato.

Analogamente, viene [*creata una*](../secgloss/d-gly.md) firma digitale del contenuto, descritta più dettagliatamente di seguito, con la chiave privata del firmatario. La chiave pubblica corrispondente, disponibile per tutti gli utenti, viene usata per verificare questa firma. La segretezza della chiave privata deve essere mantenuta perché il framework cade a pezzi dopo la compromissione della chiave privata.

Dato il tempo e le risorse sufficienti, una coppia di chiavi pubblica/privata può essere compromessa, cio' può essere individuata la chiave privata. Più lunga è la chiave, più è difficile usare la forza bruta per individuare la chiave privata. In pratica, è possibile usare chiavi sufficientemente solide per rendere impossibile determinare la chiave privata in modo adeguato, rendendo l'infrastruttura a chiave pubblica un meccanismo di sicurezza praticabile.

Una chiave privata può essere archiviata, in formato protetto, su un disco, nel qual caso può essere usata solo con quel computer specifico, a meno che non venga fisicamente spostata in un altro computer. Un'alternativa consiste nell'avere una chiave in un smart card che può essere usata in un computer diverso a condizione che abbia un lettore smart card software di supporto.

La chiave pubblica, ma non la chiave privata, del soggetto di un certificato digitale viene inclusa come parte della richiesta [*di certificato.*](../secgloss/c-gly.md) Di conseguenza, prima di effettuare la richiesta di certificato deve esistere una coppia di chiavi pubblica/privata. Tale chiave pubblica diventa parte del certificato emesso.

## <a name="the-certificate-request"></a>Richiesta di certificato

Prima dell'emissione di un certificato, [*deve essere generata*](../secgloss/c-gly.md) una richiesta di certificato. Questa richiesta si applica a un'entità, ad esempio un utente finale, un computer o un'applicazione. Per la discussione, si supponga che l'entità sia se stessa. I dettagli dell'identità sono inclusi nella richiesta di certificato. Dopo la generazione, la richiesta viene inviata a [*un'autorità di*](../secgloss/c-gly.md) certificazione (CA). La CA usa quindi le informazioni sull'identità per determinare se la richiesta soddisfa i criteri della CA per il rilascio di un certificato. Se la CA approva la richiesta, elava un certificato come entità denominata nella richiesta.

## <a name="the-certification-authority"></a>Autorità di certificazione

Prima di rilasciare il certificato, l'autorità di certificazione verifica l'identità. Quando il certificato viene emesso, l'identità viene associata al certificato, che contiene la chiave pubblica. Il certificato contiene anche la firma digitale della CA (che può essere verificata da chiunque riceva il certificato).

Poiché il certificato contiene l'identità della CA emittente, un'entità interessata che considera attendibile questa CA può estendere tale attendibilità al certificato. Il rilascio di un certificato non stabilisce una relazione di trust, ma trasferisce l'attendibilità. Se il consumer del certificato non considera attendibile la CA emittente, non considera attendibile (o almeno non deve) considerare attendibile il certificato.

Una catena di certificati firmati consente il trasferimento dell'attendibilità anche ad altre CA. In questo modo le parti che usano autorità di certificazione diverse possono comunque considerare attendibili i certificati, purché nella catena sia presente una CA comune, ovvero una CA attendibile da entrambe le parti.

## <a name="the-certificate"></a>Certificato

Oltre alla chiave pubblica e all'identità della CA emittente, il certificato emesso contiene informazioni sugli scopi della chiave e del certificato. Include inoltre il percorso dell'elenco di certificati revocati della CA e specifica il periodo di validità del certificato (date di inizio e di fine).

Supponendo che l'utente del certificato ritieni attendibile la CA emittente per il certificato, il consumer del certificato deve determinare se il certificato è ancora valido confrontando le date di inizio e di fine del certificato con l'ora corrente e verificando che il certificato non sia presente nell'elenco di certificati revocati della CA.

## <a name="the-certificate-revocation-list"></a>Elenco di revoche di certificati

Supponendo che il certificato venga usato in un periodo di tempo valido e che il consumer del certificato ritieni [](../secgloss/c-gly.md) attendibile la CA emittente, è necessario che il consumer del certificato controlli un altro elemento prima di usare il certificato: l'elenco di revoche di certificati (CRL). Il consumer di certificati controlla l'elenco CRL della CA (percorso incluso come estensione nel certificato) per assicurarsi che il certificato non sia incluso nell'elenco di certificati revocati. I CRL esistono perché in alcuni casi un certificato non è scaduto, ma non può più essere considerato attendibile. Periodicamente, la CA pubblicherà un CRL aggiornato. Gli utenti del certificato sono responsabili del confronto dei certificati con l'elenco CRL corrente prima di considerare attendibile il certificato.

## <a name="your-public-key-used-for-encryption"></a>Chiave pubblica usata per la crittografia

Se un mittente vuole crittografare un messaggio prima di inviarlo, il mittente recupera prima il certificato. Dopo che il mittente ha determinato che la CA è attendibile e che il certificato è valido e non revocato, il mittente usa la chiave pubblica (ricordare che fa parte del certificato) con algoritmi di crittografia per crittografare il messaggio di testo non crittografato in testo [](../secgloss/p-gly.md) crittografato. [](../secgloss/c-gly.md) Quando si riceve il testo crittografato, si usa la chiave privata per decrittografare il testo crittografato.

Se una terza parte intercetta il messaggio di posta elettronica crittografato, la terza parte non sarà in grado di decrittografarlo senza accedere alla [*chiave privata*](../secgloss/p-gly.md).

Si noti che la maggior parte delle attività elencate di seguito viene gestita dal software, non direttamente dall'utente.

## <a name="your-public-key-used-for-signature-verification"></a>Chiave pubblica usata per la verifica della firma

Una [*firma digitale*](../secgloss/d-gly.md) viene usata come conferma che un messaggio non è stato modificato e come conferma dell'identità del mittente del messaggio. Questa firma digitale dipende dalla chiave privata e dal contenuto del messaggio. Usando il messaggio come input e la chiave privata, gli algoritmi di crittografia creano la firma digitale. Il contenuto del messaggio non viene modificato dal processo di firma. Un destinatario può usare la chiave pubblica (dopo aver verificato la validità del certificato, la CA emittente e lo stato di revoca) per determinare se la firma corrisponde al contenuto del messaggio e per determinare se il messaggio è stato inviato dall'utente.

Se una terza parte intercetta il messaggio previsto, lo modifica (anche leggermente) e lo inoltra e la firma originale al destinatario, il destinatario, dopo l'esame del messaggio e della firma, sarà in grado di determinare che il messaggio è sospetto. Analogamente, se una terza parte crea un messaggio e lo invia con una firma digitale fasunda con la falsa origine, il destinatario sarà in grado di usare la chiave pubblica per determinare che il messaggio e la firma non corrispondono tra loro.

[*La mancata ripudio*](../secgloss/n-gly.md) è supportata anche dalle firme digitali. Se il mittente di un messaggio firmato nega l'invio del messaggio, il destinatario può usare la firma per confutare tale attestazione.

Si noti che la maggior parte delle attività elencate qui viene gestita anche dal software, non direttamente dall'utente.

## <a name="microsoft-certificate-services-role"></a>Ruolo di Servizi certificati Microsoft

Servizi certificati Microsoft ha il ruolo di rilasciare certificati o negare le richieste di certificati, come indicato dai moduli dei criteri, responsabili di garantire l'identità del richiedente del certificato. Servizi certificati offre anche la possibilità di revocare un certificato, nonché di pubblicare il CRL. Servizi certificati può anche distribuire centralmente (ad esempio, a un servizio directory) i certificati rilasciati. La possibilità di rilasciare, distribuire, revocare e gestire i certificati, insieme alla pubblicazione di CRL, offre le funzionalità necessarie per l'infrastruttura a chiave pubblica.

 

 
