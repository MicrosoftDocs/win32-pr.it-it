---
description: Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Trasformazioni protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885685"
---
# <a name="secured-transforms"></a>Trasformazioni protette

Le trasformazioni protette sono talvolta necessarie per motivi di sicurezza. Le trasformazioni protette vengono archiviate localmente nel computer dell'utente in una posizione in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura. Tali trasformazioni vengono memorizzate nella cache in questa posizione durante l'installazione o l'annuncio del pacchetto. Solo gli amministratori e il sistema locale hanno accesso in scrittura a questo percorso. Un utente non amministratore non sarà in grado di modificare il file di trasformazione. Durante le installazioni successive di [installazione su richiesta](installation-on-demand.md) o [manutenzione](maintenance-installation.md) del pacchetto, il programma di installazione usa le trasformazioni memorizzate nella cache.

Per specificare l'archiviazione di trasformazione protetta, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md), impostare la proprietà [**TRANSFORMSSECURE**](transformssecure.md) oppure passare il simbolo @ o \| nell'elenco trasformazioni. Si noti che non è possibile includere trasformazioni protette e non protette nello stesso elenco di trasformazioni. Vedere [applicazione di trasformazioni](applying-transforms.md).

La rimozione del prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni protette per il prodotto dal computer dell'utente.

Se il programma di installazione rileva che una trasformazione protetta non è disponibile localmente, tenta di ripristinare la cache di trasformazione da un'origine. Le trasformazioni protette possono essere sicure all'origine o protette-Full-Path:

-   Le [trasformazioni protette a livello di origine](secure-at-source-transforms.md) mancanti dalla cache di trasformazione locale vengono ripristinate dalla radice dell'origine del file con estensione msi.
-   Le [trasformazioni protette con percorso completo](secure-full-path-transforms.md) mancanti dalla cache di trasformazione locale vengono ripristinate dal percorso completo originale specificato dall'elenco Transforms.

 

 



