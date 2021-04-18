---
description: Viene illustrata la procedura utilizzata per archiviare una chiave di sessione.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Archiviazione di una chiave di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312796"
---
# <a name="storing-a-session-key"></a>Archiviazione di una chiave di sessione

> [!Note]  
> In questa sezione si presuppone che gli utenti dispongano di un set di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md). Le istruzioni e un esempio per la creazione di coppie di chiavi sono disponibili nel [programma C di esempio: creazione di un contenitore di chiavi e generazione di chiavi](example-c-program-creating-a-key-container-and-generating-keys.md).

 

**Per archiviare una chiave di sessione**

1.  Creare un [*BLOB di chiavi*](../secgloss/k-gly.md) semplice usando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) . Questa operazione trasferirà la chiave della sessione dal CSP allo spazio di memoria di un'applicazione. Consente di specificare che verrà utilizzata una chiave pubblica di Exchange per firmare il BLOB della chiave.
2.  Archiviare il BLOB della chiave con segno su disco. Si presuppone che tutti i dischi non siano sicuri.
3.  Quando la chiave è necessaria, leggere il BLOB della chiave dal disco.
4.  Importare di nuovo il BLOB della chiave nel CSP usando la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .

Per un esempio di creazione di una [*chiave di sessione*](../secgloss/s-gly.md) e di esportazione della chiave in un BLOB di [*chiavi semplice*](../secgloss/s-gly.md) che può essere scritto in un file su disco, vedere [esempio C Program: exporting a Session Key](example-c-program-exporting-a-session-key.md).

Questa procedura fornisce solo una sicurezza minima. Se la chiave della sessione archiviata verrà utilizzata per crittografare i dati in un secondo momento, la procedura precedente non fornirà una sicurezza adeguata.

Per garantire una maggiore sicurezza, firmare il BLOB della chiave con una chiave privata di Exchange prima di archiviarlo su disco. Quando il BLOB della chiave viene letto successivamente dal disco, la relativa firma può essere convalidata per garantire che il BLOB della chiave sia intatto.

Se il BLOB della chiave non è firmato, qualsiasi utente con accesso al disco o ad altri supporti in cui è archiviata la chiave può creare una nuova chiave di sessione.

La nuova chiave della sessione può essere crittografata con la [*chiave di scambio*](../secgloss/e-gly.md)della [*chiave pubblica*](../secgloss/p-gly.md) dell'utente originale e la nuova chiave può essere sostituita dall'originale. Se l'utente ha usato inconsapevolmente la chiave della sessione sostituita per crittografare i file e i messaggi, la persona che ha creato il tasto sostitutivo potrebbe decrittografarli facilmente.

Le firme digitali sono descritte in dettaglio in [hash e firme digitali](hashes-and-digital-signatures.md).

 

 
