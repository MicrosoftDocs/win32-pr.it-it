---
description: Transizioni
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884906"
---
# <a name="transitions"></a>Transizioni

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Una transizione è un modo per segue da una traccia video a un'altra, usando un effetto visivo come una dissolvenza o una cancellazione. Nella figura seguente viene illustrata una sequenza temporale con una transizione:

![sequenza temporale con transizione](images/timeline3.png)

L'oggetto Transition si trova nella traccia 1 e rappresenta una transizione da Track 0 a Track 1. All'inizio della transizione, il video sottoposto a rendering è interamente da Track 0 (Source A). Alla fine, il video è interamente di Track 1 (Source C). In between, l'output passa dall'origine a all'origine C. In una transizione dissolvenza, ad esempio, un'origine si dissolve progressivamente nell'altra. L'output finale è schematizzato lungo la parte inferiore dell'illustrazione.

Le transizioni non possono sovrapporsi nel tempo all'interno della stessa traccia, ma è possibile creare transizioni sovrapposte usando l'oggetto Composition, come descritto in [composizione e livelli](composition-and-layering.md).

Una transizione ha una direzione. Per impostazione predefinita, inizia dalla traccia con priorità inferiore (origine A, nell'esempio precedente) e termina in corrispondenza della traccia con priorità maggiore (origine C). In between il video è costituito da una combinazione delle due origini. Tuttavia, è possibile specificare il comportamento opposto, come illustrato nella figura seguente:

![ntrack con due transizioni](images/fade.png)

In questo caso, la prima transizione si dissolve da Track 0 Fades Track 1, che è il comportamento predefinito. La seconda transizione si dissolve da Track 1 fino a Track 0. Si noti che entrambe le transizioni si trovano nella traccia 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con i servizi di modifica DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transizioni ed effetti](transitions-and-effects.md)
</dt> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



