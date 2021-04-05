---
title: Ricerca nel catalogo globale
description: Active Directory Domain Services dispone anche di un catalogo globale (GC), che contiene una replica parziale di tutti gli oggetti nella directory.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- ricerca nel catalogo globale Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707558"
---
# <a name="searching-the-global-catalog"></a>Ricerca nel catalogo globale

Active Directory Domain Services dispone anche di un catalogo globale (GC), che contiene una replica parziale di tutti gli oggetti nella directory. Contiene anche le repliche parziali dei contenitori dello schema e della configurazione. Uno o più controller di dominio in un dominio possono conservare una copia del catalogo globale. Per ulteriori informazioni sull'associazione a un catalogo globale, vedere [associazione al catalogo globale](binding-to-the-global-catalog.md).

Il catalogo globale include una replica di ogni oggetto in Active Directory Domain Services, ma con un numero ridotto di attributi. Gli attributi nel catalogo globale sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente, i nomi di accesso e così via. Gli attributi del catalogo globale includono anche quelli necessari per individuare una replica completa dell'oggetto. Il catalogo globale consente agli utenti di trovare rapidamente oggetti di interesse senza conoscere il dominio che li contiene e senza richiedere uno spazio dei nomi esteso contiguo nell'organizzazione. ovvero, è possibile eseguire ricerche nell'intera foresta.

Se quindi si esegue l'associazione a un oggetto nel catalogo globale, si eseguirà la ricerca dell'oggetto e dell'intera gerarchia sottostante, senza dover passare a un altro server. Tuttavia, la ricerca può utilizzare solo un filtro di query che contiene le proprietà nel catalogo globale e può recuperare solo le proprietà nel catalogo globale.

La ricerca nel catalogo globale presenta i vantaggi seguenti:

-   Il catalogo globale consente di eseguire ricerche nell'intera foresta o in qualsiasi parte della foresta, nonché nei contenitori dello schema e della configurazione.
-   Il catalogo globale consente di eseguire una ricerca completa su un singolo server. Non è richiesto alcun riferimento o inseguimento del riferimento.

La ricerca nel catalogo globale presenta gli svantaggi seguenti:

-   Il catalogo globale contiene un piccolo subset delle proprietà per ogni oggetto. Se il filtro di query include proprietà non presenti nel catalogo globale, la query valuterà le espressioni che contengono tali proprietà come false. Se si specificano proprietà del catalogo non globali nell'elenco di proprietà da restituire, tali proprietà non vengono recuperate.
-   Per eseguire una ricerca nel catalogo globale, è necessario che sia disponibile un controller di dominio che contiene un catalogo globale. Se non è disponibile, non è possibile eseguire una ricerca nel catalogo globale.
-   Il catalogo globale è di sola lettura. Ciò significa che non è possibile eseguire l'associazione a un oggetto nel catalogo globale per creare, modificare o eliminare oggetti.

 

 




