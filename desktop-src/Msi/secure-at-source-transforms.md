---
description: Le trasformazioni sicure all'origine devono disporre di un'origine che si trova nella radice dell'origine per il pacchetto.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Trasformazioni protette a livello di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885686"
---
# <a name="secure-at-source-transforms"></a>Trasformazioni protette a livello di origine

Le trasformazioni sicure all'origine devono disporre di un'origine che si trova nella radice dell'origine per il pacchetto. Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura. Se la copia locale della trasformazione diventa non disponibile, il programma di installazione cerca un'origine per ripristinare la cache. Il metodo è identico a quello di ricerca nell'elenco di origine di un file con estensione msi. Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md). La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per il prodotto dal computer dell'utente.

Per applicare le trasformazioni sicure all'origine durante l'installazione di un pacchetto, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) oppure fare in modo che @ il primo carattere passato nell'elenco di trasformazione. Ogni trasformazione deve essere indicata da un nome di file e deve trovarsi nella radice dell'origine del pacchetto. Se una delle trasformazioni non si trova nella radice dell'origine del pacchetto, l'installazione non riesce. Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).

 

 



