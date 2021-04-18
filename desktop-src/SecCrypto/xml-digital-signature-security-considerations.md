---
description: Le applicazioni che firmano e verificano le firme digitali XML devono essere scritte secondo le seguenti procedure consigliate per evitare attacchi di tipo Denial of Service, perdita di dati e compromissione di informazioni private.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Considerazioni sulla sicurezza della firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e54b4c5f3f863e0bc84172a7507bfe8609e2df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316130"
---
# <a name="xml-digital-signature-security-considerations"></a>Considerazioni sulla sicurezza della firma digitale XML

Le applicazioni che firmano e verificano le firme digitali XML devono essere scritte secondo le seguenti procedure consigliate per evitare attacchi di tipo Denial of Service, perdita di dati e compromissione di informazioni private. L'elenco seguente fornisce indicazioni generali; Tuttavia, gli sviluppatori sono invitati a eseguire analisi di sicurezza aggiuntive specifiche per le applicazioni e a esaminare le più recenti procedure consigliate pubblicate da W3C.

-   [Verificare l'attendibilità della chiave di firma](#verify-trust-of-the-signing-key)
-   [Verificare prima la chiave di firma e convalidare SignedInfo, quindi convalidare i riferimenti](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Usare il set minimo di algoritmi di canonizzazione e le trasformazioni necessarie](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Assicurarsi che gli URI di destinazione puntino alle destinazioni nell'ambito previsto](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Verificare che i dati utilizzati dall'applicazione siano verificati dalla firma](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Segui le procedure di crittografia migliori](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Verificare l'attendibilità della chiave di firma

Verificare che la chiave di firma sia attendibile verificando il certificato [*X. 509*](../secgloss/x-gly.md) corrispondente (e la catena di certificati) incluso nel messaggio firmato. In alternativa, è possibile stabilire una relazione di trust con la chiave di firma in modo fuori banda, ad esempio un amministratore che configura un set di chiavi attendibili o un'applicazione che esegue query su un servizio attendibile su un canale sicuro.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Verificare prima la chiave di firma e convalidare SignedInfo, quindi convalidare i riferimenti

Verificare l'attendibilità nella chiave di firma e l'integrità dell'elemento **SignedInfo** prima di convalidare i riferimenti. Analogamente, le applicazioni devono convalidare gli elementi del **manifesto** prima di risolvere i riferimenti contenuti negli elementi del **manifesto** . Gli elementi di **riferimento** consentono di specificare gli URI di destinazione, le trasformazioni e gli algoritmi di canonizzazione. Se non vengono convalidati, questi campi possono essere potenzialmente utilizzati per creare attacchi di tipo Denial of Service, perdita di dati o altri attacchi.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Usare il set minimo di algoritmi di canonizzazione e le trasformazioni necessarie

XSLT e XPATH non devono essere usati all'interno di elementi non autenticati, ad esempio le **informazioni sui dati**. Se un'applicazione richiede l'uso di XPath, vincolare il set di espressioni XPATH consentite solo a quelle che usano il predecessore o gli assi self e non calcolano il valore stringa degli elementi. Per impostazione predefinita, CryptXML supporta un set limitato di algoritmi di canonizzazione (vedere gli URI supportati negli [algoritmi di crittografia della firma digitale XML](xml-digital-signature-cryptographic-algorithms.md)). Gli sviluppatori possono implementare trasformazioni o algoritmi di canonizzazione aggiuntivi da usare all'interno dell'applicazione. Tuttavia, l'uso di algoritmi complessi consente di creare attacchi di tipo Denial of Service o di suddividere le caratteristiche di ripudio di una firma. Nei casi in cui le trasformazioni sono richieste dall'applicazione, limitare il numero di trasformazioni che è possibile specificare per riferimento al numero più alto richiesto dall'applicazione. Questa pratica attenua gli attacchi Denial of Service in base all'utilizzo eccessivo delle trasformazioni.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Assicurarsi che gli URI di destinazione puntino alle destinazioni nell'ambito previsto

Le applicazioni devono limitare gli URI di destinazione all'ambito più piccolo richiesto dall'applicazione. Ad esempio, è possibile che gli URI puntino a destinazioni all'interno dello stesso documento, i file in una directory di destinazione specifica o i percorsi di rete all'interno di un dominio DNS specifico. Gli URI impostati da un utente malintenzionato in modo che punti al di fuori del dominio previsto potrebbero causare il recupero di contenuti dannosi da parte di un'applicazione, l'invio di richieste HTTP dannose (possibilmente contenenti stringhe di query) o l'autenticazione di applicazioni a server dannosi.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Verificare che i dati utilizzati dall'applicazione siano verificati dalla firma

Se l'applicazione convalida la chiave di firma e gli elementi **SignedInfo** e **Reference** , ma l'applicazione utilizza dati importanti a cui non fa riferimento la firma, la firma non fornisce una protezione significativa. Il significato semantico di una firma può variare in base alla posizione della firma all'interno del documento. Le applicazioni sono incoraggiate a verificare la posizione della firma all'interno di un documento. Controllare anche la posizione dei nomi di dati e di elementi a cui si fa riferimento per attenuare gli attacchi di sostituzione e di wrapping.

## <a name="follow-best-cryptographic-practices"></a>Segui le procedure di crittografia migliori

Gli algoritmi di crittografia diventano più vulnerabili nel tempo man mano che vengono individuati nuovi attacchi e la potenza di calcolo diventa disponibile. Non codificare gli identificatori di algoritmi di crittografia o le dimensioni delle chiavi nelle applicazioni. Per un elenco più completo delle procedure di crittografia ottimali, vedere Michael Howard e Steve Lipner, "SDL Minimum Cryptography Standards" nel *ciclo di vita dello sviluppo della sicurezza* (Redmond, Washington: Microsoft Press, 2006), 251-258.

Altre procedure consigliate sono disponibili nel sito Web W3C: https://www.w3.org .

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.

 

 

 
