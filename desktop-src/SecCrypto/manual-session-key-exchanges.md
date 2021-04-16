---
description: Viene illustrato come inviare un messaggio crittografato.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Scambi manuali di chiavi di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563224"
---
# <a name="manual-session-key-exchanges"></a>Scambi manuali di chiavi di sessione

> [!Note]  
> La procedura descritta in questa sezione presuppone che gli utenti (o i client CryptoAPI) dispongano già di un proprio set di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md) e abbiano ottenuto anche le rispettive [*chiavi pubbliche*](../secgloss/p-gly.md).

 

Nella figura seguente viene illustrato come utilizzare questa procedura per inviare un messaggio crittografato.

![invio di un messaggio crittografato](images/capi04.png)

Questo approccio è vulnerabile ad almeno una forma comune di attacco. Un intercettatore può acquisire copie di uno o più messaggi crittografati e le chiavi crittografate. Quindi, in un secondo momento, l'intercettatore può inviare uno di questi messaggi al ricevitore e il ricevitore non avrà alcun modo per conoscere il messaggio non provenire direttamente dal mittente originale. Questo rischio può essere ridotto impostando il timestamp di tutti i messaggi o usando i numeri di serie.

Il modo più semplice per inviare messaggi crittografati a un altro utente consiste nell'inviare il messaggio crittografato con una chiave di sessione casuale insieme alla chiave di sessione crittografata con la chiave [*pubblica di scambio delle chiavi*](../secgloss/k-gly.md)del destinatario.

Di seguito sono riportati i passaggi per l'invio di una chiave di sessione crittografata.

**Per inviare una chiave di sessione crittografata**

1.  Creare una [*chiave di sessione*](../secgloss/s-gly.md) casuale usando la funzione [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .
2.  Crittografare il messaggio utilizzando la chiave della sessione. Questa procedura è illustrata in [crittografia e decrittografia dei dati](data-encryption-and-decryption.md).
3.  Esportare la chiave della sessione in un [*BLOB di chiavi*](../secgloss/k-gly.md) con la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , specificando che la chiave deve essere crittografata con la chiave pubblica di scambio delle chiavi dell'utente di destinazione.
4.  Inviare il messaggio crittografato e il BLOB della chiave crittografata all'utente di destinazione.
5.  L'utente di destinazione importa il BLOB della chiave nel suo CSP usando la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) . La chiave della sessione verrà decrittografata automaticamente, purché sia stata specificata la chiave pubblica per lo scambio delle chiavi dell'utente di destinazione nel passaggio 3.
6.  L'utente di destinazione può quindi decrittografare il messaggio utilizzando la chiave della sessione, seguendo la procedura descritta in [crittografia dei dati e decrittografia](data-encryption-and-decryption.md).

 

 
