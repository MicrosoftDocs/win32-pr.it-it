---
description: Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Trasformazioni protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07c36b70827c301117bff7d98b30aae2990efb80f892bda24b0be35cbba5316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040841"
---
# <a name="secured-transforms"></a>Trasformazioni protette

Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza. Le trasformazioni protette vengono archiviate localmente nel computer dell'utente in una posizione in cui, in un file system sicuro, l'utente non ha accesso in scrittura. Tali trasformazioni vengono memorizzate nella cache in questo percorso durante l'installazione o l'annuncio del pacchetto. Solo gli amministratori e il sistema locale hanno accesso in scrittura a questo percorso. Un utente non amministratore non sarebbe in grado di modificare il file di trasformazione. Durante le [successive installazioni su richiesta](installation-on-demand.md) [o](maintenance-installation.md) di manutenzione del pacchetto, il programma di installazione usa le trasformazioni memorizzate nella cache.

Per specificare l'archiviazione protetta delle trasformazioni, impostare il criterio [TransformsSecure](transformssecure-policy.md), impostare la [**proprietà TRANSFORMSSECURE**](transformssecure.md) o passare il simbolo @ o \| nell'elenco delle trasformazioni. Si noti che non è possibile includere trasformazioni protette e non protette nello stesso elenco di trasformazioni. Vedere [Applicazione di trasformazioni.](applying-transforms.md)

La rimozione del prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni protette per tale prodotto dal computer dell'utente.

Se il programma di installazione rileva che una trasformazione protetta non è disponibile in locale, tenta di ripristinare la cache delle trasformazioni da un'origine. Le trasformazioni sicure possono essere secure-at-source o secure-full-path:

-   [Le trasformazioni secure-at-source](secure-at-source-transforms.md) mancanti nella cache delle trasformazioni locali vengono ripristinate dalla radice dell'origine del file .msi.
-   [Le trasformazioni secure-full-path](secure-full-path-transforms.md) mancanti nella cache delle trasformazioni locali vengono ripristinate dal percorso completo originale specificato dall'elenco delle trasformazioni.

 

 



