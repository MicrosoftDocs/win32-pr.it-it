---
description: Le chiavi asimmetriche, note anche come coppie di chiavi pubblica/privata, vengono usate per la crittografia asimmetrica. La crittografia asimmetrica viene usata principalmente per crittografare e decrittografare le chiavi di sessione e le firme digitali. La crittografia asimmetrica usa algoritmi di crittografia a chiave pubblica.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Chiavi asimmetriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901473"
---
# <a name="asymmetric-keys"></a>Chiavi asimmetriche

[*Le chiavi asimmetriche,*](../secgloss/a-gly.md)note anche [*come coppie di chiavi pubblica/privata,*](../secgloss/p-gly.md)vengono usate per la crittografia asimmetrica. La crittografia asimmetrica viene usata principalmente per crittografare e [*decrittografare le chiavi*](../secgloss/s-gly.md) di sessione [*e le firme digitali*](../secgloss/d-gly.md). La crittografia asimmetrica [*usa algoritmi di crittografia*](../secgloss/p-gly.md) a chiave pubblica.

Gli algoritmi a chiave pubblica usano due chiavi diverse: [*una chiave pubblica*](../secgloss/p-gly.md) e una chiave [*privata*](../secgloss/p-gly.md). Il membro della chiave privata della coppia deve essere mantenuto privato e protetto. La chiave pubblica, tuttavia, può essere distribuita a chiunque la richiede. La chiave pubblica di una coppia di chiavi viene spesso distribuita tramite un [*certificato digitale.*](../secgloss/c-gly.md) Quando una chiave di una coppia di chiavi viene usata per crittografare un messaggio, l'altra chiave di tale coppia è necessaria per decrittografare il messaggio. Pertanto, se la chiave pubblica dell'utente A viene usata per crittografare i dati, solo l'utente A (o un utente che ha accesso alla chiave privata dell'utente A) può decrittografare i dati. Se la chiave privata dell'utente A viene usata per crittografare un dato, solo la chiave pubblica dell'utente A decrittografa i dati, a indicare che l'utente A (o un utente con accesso alla chiave privata dell'utente A) ha usato la crittografia.

Se la chiave privata viene usata per firmare un messaggio, è necessario usare la chiave pubblica di tale coppia per convalidare la firma. Ad esempio, se Alice vuole inviare a un utente un messaggio con firma digitale, firma il messaggio con la propria chiave privata e l'altra persona può verificare la firma usando la chiave pubblica. Poiché presumibilmente solo Alice ha accesso alla propria chiave privata, il fatto che la firma possa essere verificata con la chiave pubblica di Alice indica che Alice ha creato la firma.

Sfortunatamente, gli algoritmi a chiave pubblica sono molto lenti, circa 1.000 volte più lenti degli algoritmi simmetrici. Non è pratico usarli per crittografare grandi quantità di dati. In pratica, gli algoritmi a chiave pubblica vengono usati per crittografare le [*chiavi di sessione*](../secgloss/s-gly.md). [*Gli algoritmi simmetrici vengono usati*](../secgloss/s-gly.md) per la crittografia/decrittografia della maggior parte dei dati.

Analogamente, poiché la firma di un messaggio, in effetti, crittografa il messaggio, non è pratico usare algoritmi di firma a chiave pubblica per firmare messaggi di grandi dimensioni. Viene invece creato un [*hash*](../secgloss/h-gly.md) a lunghezza fissa del messaggio e il valore hash è firmato. Per altre informazioni, vedere [Hash e firme digitali.](hashes-and-digital-signatures.md)

Ogni utente ha in genere due [*coppie di chiavi pubblica/privata.*](../secgloss/p-gly.md) Una coppia di chiavi viene usata per crittografare le chiavi di sessione e l'altra per creare [*firme digitali.*](../secgloss/d-gly.md) Questi sono noti rispettivamente come [*coppia di chiavi*](../secgloss/k-gly.md) di scambio delle chiavi e coppia di chiavi [*di*](../secgloss/s-gly.md)firma.

Si noti che anche se i contenitori di chiavi creati dalla maggior parte [*dei*](../secgloss/c-gly.md) provider del servizio di crittografia contengono due coppie di chiavi, questa operazione non è necessaria. Alcuni CSP non archiviano coppie [*di chiavi mentre*](../secgloss/k-gly.md) altri CSP archiviano più di due coppie.

Tutte le chiavi in CryptoAPI vengono archiviate all'interno di CSP. I provider di servizi di configurazione sono anche responsabili della creazione delle chiavi, dell'eliminazione e dell'uso delle chiavi per eseguire un'ampia gamma di operazioni di crittografia. L'esportazione di chiavi da CSP in modo che possano essere inviate ad altri utenti è descritta in Crittografia delle chiavi Archiviazione [e Exchange](cryptographic-key-storage-and-exchange.md).

 

 
