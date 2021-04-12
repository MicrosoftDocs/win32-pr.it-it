---
title: Chiamate annidate a SRSetRestorePoint
description: In questo argomento viene descritto il supporto per le chiamate annidate a SRSetRestorePoint tramite i tipi di evento BEGIN NESTED \_ \_ System change \_ e End \_ Nested \_ System \_ Change.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221533"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Chiamate annidate a SRSetRestorePoint

In questo argomento viene descritto il supporto per le chiamate annidate a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) tramite i tipi di evento Begin nested \_ System change \_ \_ e End \_ Nested \_ System \_ Change.

Quando si usano questi tipi di evento, le applicazioni possono chiamare [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) in modo sicuro. La prima chiamata alla funzione crea un punto di ripristino. Le successive chiamate annidate alla funzione non creano punti di ripristino. Si supponga, ad esempio, che un'applicazione effettua le chiamate seguenti a **SRSetRestorePoint**:<dl> Per il punto di ripristino A con dwEventType = inizio \_ \_ modifica sistema annidato \_  
Per il punto di ripristino B con dwEventType = BEGIN \_ Nested \_ System \_ Change  
Per il punto di ripristino B con dwEventType = END \_ Nested \_ System \_ Change  
Per il punto di ripristino A con dwEventType = fine \_ \_ modifica sistema annidato \_  
</dl>

La seconda chiamata non crea un nuovo punto di ripristino perché la chiamata è annidata.

 

 




