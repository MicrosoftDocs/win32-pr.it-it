---
description: Poiché il numero di certificati, elenchi di revoche di certificati (CRL) e elenco di certificati attendibili (scopi consentiti) nella raccolta di un utente cresce, l'organizzazione di tali certificati diventa un problema.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Archivi della raccolta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883802"
---
# <a name="collection-stores"></a>Archivi della raccolta

Poiché il numero di [*certificati*](../secgloss/c-gly.md), [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) e [*elenco di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti) nella raccolta di un utente cresce, l'organizzazione di tali certificati diventa un problema. Una possibile soluzione consiste nel creare archivi certificati separati per gestire tipi diversi di certificati. Questa soluzione crea un nuovo problema perché un'applicazione potrebbe dover eseguire ricerche in diversi archivi diversi per trovare un certificato specifico. Questo problema viene risolto utilizzando gli archivi logici o di raccolta.

Un archivio [*logico*](../secgloss/l-gly.md) e un archivio certificati raccolta sono gruppi di archivi fisici che vengono visualizzati in un'applicazione come singolo archivio. È possibile cercare o enumerare tutti gli archivi membri di un archivio logico o di una raccolta con una singola chiamata di funzione a [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) o [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).

L'utilizzo di archivi logici o di raccolte fornisce anche la flessibilità che è difficile ottenere con i record cartacei. Un certificato in un singolo archivio fisico potrebbe dover essere membro di più gruppi logici diversi. Pertanto, un singolo archivio fisico può essere un membro di più di un archivio logico o di raccolta, come illustrato nella figura seguente.

![archivi della raccolta](images/mancert.png)

Questa illustrazione presenta i concetti di base dell'archivio certificati logici seguenti:

-   Un archivio certificati della raccolta include un puntatore al primo blocco del puntatore per l'archivio della raccolta.
-   Ogni blocco del puntatore di un archivio di raccolta dispone di un puntatore a un archivio di pari livello e un puntatore al successivo blocco del puntatore della raccolta.
-   Ogni archivio di pari livello in una raccolta è un archivio certificati fisico semplice.
-   Un archivio certificati semplice può essere un archivio di pari livello di un membro in molti archivi di raccolta diversi.
-   I certificati aggiunti a un archivio di raccolta vengono fisicamente aggiunti a uno degli archivi di pari livello nella raccolta.
-   È possibile accedere ai certificati in un archivio di pari livello da qualsiasi archivio di raccolta in cui è membro l'archivio di pari livello.

Gli archivi di raccolta vengono compilati all'interno di un'applicazione aprendo un archivio di raccolta tramite [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) e quindi utilizzando [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) per aggiungere un archivio di pari livello aperto all'archivio della raccolta. Un archivio di pari livello può essere eliminato da un archivio di raccolta chiamando [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).

 

 
