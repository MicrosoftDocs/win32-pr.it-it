---
description: Per le trasformazioni con percorso completo è necessario che un'origine si trovi nel percorso completo specificato nella proprietà Transforms.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Trasformazioni protette con percorso completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530301"
---
# <a name="secure-full-path-transforms"></a>Trasformazioni protette con percorso completo

Per le trasformazioni con percorso completo è necessario che un'origine si trovi nel percorso completo specificato nella proprietà [**TRANSforms**](transforms.md) . Quando il pacchetto viene installato o annunciato, il programma di installazione salva le trasformazioni in una cache in cui, in un file system protetto, l'utente non dispone dell'accesso in scrittura. Se la copia locale della trasformazione non è più disponibile, può ripristinare solo la cache usando il percorso specificato. La rimozione di un prodotto da parte di qualsiasi utente rimuove tutte le trasformazioni sicure per il prodotto dal computer dell'utente.

Per applicare le trasformazioni Secure-Full-Paths durante l'installazione di un pacchetto, impostare il [criterio TRANSFORMSSECURE](transformssecure-policy.md) o la proprietà [**TRANSFORMSSECURE**](transformssecure.md) o rendere \| il primo carattere passato nell'elenco di trasformazione. I percorsi completi dell'origine di ogni trasformazione devono essere passati nella stringa Transforms. Se nell'elenco sono presenti percorsi relativi, l'installazione non riesce. Non è necessario che l'origine della trasformazione si trovi con l'origine del pacchetto.

 

 



