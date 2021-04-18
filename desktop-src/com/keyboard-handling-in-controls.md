---
title: Gestione della tastiera nei controlli
description: Gestione della tastiera nei controlli
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298935"
---
# <a name="keyboard-handling-in-controls"></a>Gestione della tastiera nei controlli

Il supporto per la gestione della tastiera per le funzionalità seguenti è fortemente consigliato, anche se è noto che non è applicabile a tutti i contenitori.

-   Supporto per i \_ bit di stato OLEMISC ACTSLIKELABEL e OLEMISC \_ ACTSLIKEBUTTON.
-   Implementando la proprietà di ambiente DisplayAsDefault, se esistente, può restituire **false**.
-   Implementazione della gestione delle schede, incluso l'ordine di tabulazione.

Alcuni contenitori utilizzeranno i controlli ActiveX negli scenari tradizionali dei documenti composti. Un foglio di calcolo, ad esempio, può consentire a un utente di incorporare un controllo ActiveX in un foglio di lavoro. In questi scenari, il contenitore eseguirebbe la gestione della tastiera in modo diverso, perché l'interfaccia della tastiera deve rimanere coerente con le aspettative dell'utente di un foglio di calcolo. La documentazione relativa a tali prodotti deve informare gli utenti sulle differenze nella gestione dei controlli in questi diversi scenari. Gli altri contenitori dovrebbero tentare di rispettare correttamente le funzionalità sopra indicate, inclusa la gestione dei tasti di scelta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 




