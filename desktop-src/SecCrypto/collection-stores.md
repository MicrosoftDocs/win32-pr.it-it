---
description: Con l'aumentare del numero di certificati, elenchi di revoche di certificati (CRL) e elenchi di certificati attendibili (CCL) nella raccolta di un utente, l'organizzazione di tali certificati diventa un problema.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Archivi di raccolta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d783aafe6d0ff22cd990195f6bce5ce433f2f01595bed2cf20c5c41ea3a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876916"
---
# <a name="collection-stores"></a>Archivi di raccolta

Con l'aumentare del numero di [*certificati,*](../secgloss/c-gly.md)degli elenchi di [*revoche*](../secgloss/c-gly.md) di certificati [](../secgloss/c-gly.md) (CRL) e degli elenchi di certificati attendibili (CCL) nella raccolta di un utente, l'organizzazione di tali certificati diventa un problema. Una possibile soluzione consiste nel creare archivi certificati separati per mantenere diversi tipi di certificati. Questa soluzione crea un nuovo problema perché un'applicazione potrebbe dover eseguire ricerche in diversi archivi per trovare un certificato specifico. L'uso di archivi logici o di raccolta risolve questo problema.

Un [*archivio logico e*](../secgloss/l-gly.md) un archivio certificati di raccolta sono gruppi di archivi fisici che vengono visualizzati in un'applicazione come archivio singolo. È possibile cercare o enumerare tutti gli archivi membri di un archivio logico o di raccolta con una singola chiamata di funzione a [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) o [**CertEnumCertificatesInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)

L'uso di archivi logici o di raccolta offre anche una flessibilità difficile da ottenere con i record cartacei. Un certificato in un singolo archivio fisico potrebbe dover essere membro di diversi gruppi logici. Pertanto, un singolo archivio fisico può essere membro di più archivi logici o di raccolta, come illustrato nella figura seguente.

![archivi di raccolta](images/mancert.png)

Questa illustrazione presenta i concetti di base dell'archivio certificati logico seguenti:

-   Un archivio certificati della raccolta ha un puntatore al primo blocco di puntatori per tale archivio raccolta.
-   Ogni blocco di puntatore di un archivio di raccolta ha un puntatore a un archivio di pari livello e un puntatore al blocco di puntatore successivo della raccolta.
-   Ogni archivio di pari livello in una raccolta è un semplice archivio certificati fisico.
-   Un archivio certificati semplice può essere un archivio di pari livello membro in molti archivi raccolta diversi.
-   I certificati aggiunti a un archivio di raccolta vengono aggiunti fisicamente a uno degli archivi di pari livello nella raccolta.
-   I certificati in un archivio di pari livello sono accessibili da qualsiasi archivio di raccolta in cui l'archivio di pari livello è membro.

Gli archivi di raccolta vengono compilati all'interno di un'applicazione aprendo un archivio di raccolta usando [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) e quindi [**usando CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) per aggiungere un archivio di pari livello aperto all'archivio di raccolta. Un archivio di pari livello può essere eliminato da un archivio di raccolta chiamando [**CertRemoveStoreFromCollection.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection)

 

 
