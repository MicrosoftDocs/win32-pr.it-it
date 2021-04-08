---
description: Per la crittografia asimmetrica vengono utilizzate chiavi asimmetriche, note anche come coppie di chiavi pubblica/privata. La crittografia asimmetrica viene utilizzata principalmente per crittografare e decrittografare le chiavi di sessione e le firme digitali. La crittografia asimmetrica usa gli algoritmi di crittografia a chiave pubblica.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Chiavi asimmetriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c475b1d0260bd20495d28ab542ca18c0d1cefa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759629"
---
# <a name="asymmetric-keys"></a>Chiavi asimmetriche

Per la crittografia asimmetrica vengono utilizzate [*chiavi asimmetriche*](../secgloss/a-gly.md), note anche come [*coppie di chiavi pubblica/privata*](../secgloss/p-gly.md). La crittografia asimmetrica viene utilizzata principalmente per crittografare e decrittografare le [*chiavi di sessione*](../secgloss/s-gly.md) e le [*firme digitali*](../secgloss/d-gly.md). La crittografia asimmetrica usa gli algoritmi di [*crittografia a chiave pubblica*](../secgloss/p-gly.md) .

Gli algoritmi a chiave pubblica usano due chiavi diverse: una [*chiave pubblica*](../secgloss/p-gly.md) e una [*chiave privata*](../secgloss/p-gly.md). Il membro della chiave privata della coppia deve essere mantenuto privato e sicuro. La chiave pubblica, tuttavia, può essere distribuita a chiunque lo richieda. La chiave pubblica di una coppia di chiavi viene spesso distribuita per mezzo di un [*certificato digitale*](../secgloss/c-gly.md). Quando una chiave di una coppia di chiavi viene utilizzata per crittografare un messaggio, per decrittografare il messaggio è necessaria l'altra chiave della coppia. Se quindi si usa la chiave pubblica dell'utente a per crittografare i dati, è possibile decrittografare i dati solo l'utente A (o un utente che ha accesso alla chiave privata dell'utente a). Se la chiave privata dell'utente a viene usata per crittografare un dato, solo la chiave pubblica dell'utente A dedurrà i dati, in modo che l'utente A (o un utente con accesso alla chiave privata dell'utente A) abbia fatto la crittografia.

Se la chiave privata viene utilizzata per firmare un messaggio, è necessario utilizzare la chiave pubblica della coppia per convalidare la firma. Ad esempio, se Alice desidera inviare un messaggio con firma digitale, firma il messaggio con la chiave privata e l'altra persona può verificare la firma usando la chiave pubblica. Dal momento che solo Alice ha accesso alla propria chiave privata, il fatto che la firma possa essere verificata con la chiave pubblica di Alice indica che Alice ha creato la firma.

Sfortunatamente, gli algoritmi a chiave pubblica sono molto lenti, circa 1.000 volte più lente degli algoritmi simmetrici. Non è pratico usarli per crittografare grandi quantità di dati. In pratica, gli algoritmi a chiave pubblica vengono usati per crittografare le [*chiavi di sessione*](../secgloss/s-gly.md). Gli [*algoritmi simmetrici*](../secgloss/s-gly.md) vengono usati per la crittografia/decrittografia della maggior parte dei dati.

Analogamente, poiché la firma di un messaggio, in effetti, crittografa il messaggio, non è pratico usare gli algoritmi di firma a chiave pubblica per firmare messaggi di grandi dimensioni. Viene invece creato un [*hash*](../secgloss/h-gly.md) a lunghezza fissa del messaggio e il valore hash è firmato. Per altre informazioni, vedere [hash e firme digitali](hashes-and-digital-signatures.md).

Ogni utente ha in genere due [*coppie di chiavi pubblica/privata*](../secgloss/p-gly.md). Una coppia di chiavi viene usata per crittografare le chiavi di sessione e l'altra per creare [*firme digitali*](../secgloss/d-gly.md). Queste sono note rispettivamente come [*coppia*](../secgloss/k-gly.md) di chiavi di scambio delle chiavi e [*coppia di chiavi di firma*](../secgloss/s-gly.md).

Si noti che anche se i contenitori di chiavi creati dalla maggior parte dei [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) contengono due coppie di chiavi, questa operazione non è obbligatoria. Alcuni CSP non archiviano [*coppie di chiavi*](../secgloss/k-gly.md) mentre altri DSN archiviano più di due coppie.

Tutte le chiavi in CryptoAPI sono archiviate all'interno di CSP. I CSP sono anche responsabili della creazione delle chiavi, della loro eliminazione e della loro utilizzo per eseguire varie operazioni crittografiche. L'esportazione delle chiavi dal CSP in modo che possano essere inviate ad altri utenti viene discussa in [archiviazione chiavi crittografiche ed Exchange](cryptographic-key-storage-and-exchange.md).

 

 
