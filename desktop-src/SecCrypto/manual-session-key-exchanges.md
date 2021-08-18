---
description: Illustra come inviare un messaggio crittografato.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Scambi manuali di chiavi di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c9f7338b40ed1675b2186e478c8c124719b376889ce691d305e246016e0d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425596"
---
# <a name="manual-session-key-exchanges"></a>Scambi manuali di chiavi di sessione

> [!Note]  
> La procedura descritta in questa sezione presuppone che gli utenti (o i client CryptoAPI) possiedano già un proprio set di coppie di chiavi [*pubblica/privata*](../secgloss/p-gly.md) e che si siano ottenute anche le chiavi pubbliche [*reciproche.*](../secgloss/p-gly.md)

 

Nella figura seguente viene illustrato come utilizzare questa procedura per inviare un messaggio crittografato.

![invio di un messaggio crittografato](images/capi04.png)

Questo approccio è vulnerabile ad almeno una forma comune di attacco. Un eavesdropper può acquisire copie di uno o più messaggi crittografati e delle chiavi crittografate. Successivamente, l'eavesdropper può inviare uno di questi messaggi al ricevitore e il ricevitore non sarà in grado di sapere che il messaggio non è stato ricevuto direttamente dal mittente originale. Questo rischio può essere ridotto contrassegnando tutti i messaggi o usando i numeri di serie.

Il modo più semplice per inviare messaggi crittografati a un altro utente è inviare il messaggio crittografato con una chiave di sessione casuale insieme alla chiave di sessione crittografata con la chiave pubblica di scambio della chiave del [*ricevitore.*](../secgloss/k-gly.md)

Di seguito sono riportati i passaggi per l'invio di una chiave di sessione crittografata.

**Per inviare una chiave di sessione crittografata**

1.  Creare una chiave [*di sessione casuale*](../secgloss/s-gly.md) usando la [**funzione CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
2.  Crittografare il messaggio usando la chiave di sessione. Questa procedura è descritta in [Crittografia dei dati e decrittografia.](data-encryption-and-decryption.md)
3.  Esportare la chiave di sessione in un [*BLOB*](../secgloss/k-gly.md) di chiavi con la funzione [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) specificando che la chiave deve essere crittografata con la chiave pubblica di scambio delle chiavi dell'utente di destinazione.
4.  Inviare sia il messaggio crittografato che il BLOB della chiave crittografata all'utente di destinazione.
5.  L'utente di destinazione importa il BLOB della chiave nel CSP usando la [**funzione CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) In questo modo la chiave di sessione verrà decrittografato automaticamente, a condizione che nel passaggio 3 sia stata specificata la chiave pubblica per lo scambio di chiavi dell'utente di destinazione.
6.  L'utente di destinazione può quindi decrittografare il messaggio usando la chiave di sessione, seguendo la procedura descritta in Crittografia dei dati [e decrittografia.](data-encryption-and-decryption.md)

 

 
