---
description: Transizioni
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7511a010de60cdd87907b4ad7faa59963d3f0c6037dce3adc8fc58fa1c0a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078703"
---
# <a name="transitions"></a>Transizioni

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Una transizione è un modo per passare da una traccia video a un'altra, usando un effetto visivo come una dissolvenza o una cancellazione. La figura seguente mostra una sequenza temporale con una transizione:

![sequenza temporale con transizione](images/timeline3.png)

L'oggetto di transizione si trova sulla traccia 1 e rappresenta una transizione dalla traccia 0 alla traccia 1. All'inizio della transizione, il video sottoposto a rendering è interamente dalla traccia 0 (origine A). Alla fine, il video è interamente dalla traccia 1 (origine C). In mezzo, l'output passa dall'origine A all'origine C. Ad esempio, in una transizione di dissolvenza, un'origine si dissolve progressivamente verso l'altra. L'output finale viene schematizzato nella parte inferiore dell'illustrazione.

Le transizioni non possono sovrapporsi nel tempo all'interno della stessa traccia, ma è possibile creare transizioni sovrapposte usando l'oggetto composizione, come descritto in [Composizione e sovrapposizione.](composition-and-layering.md)

Una transizione ha una direzione. Per impostazione predefinita, inizia dalla traccia con priorità inferiore (origine A, nell'esempio precedente) e termina in corrispondenza della traccia con priorità più alta (origine C). Nel mezzo, il video è una combinazione delle due origini. È tuttavia possibile specificare il comportamento opposto, come illustrato nella figura seguente:

![ntrack con due transizioni](images/fade.png)

In questo caso, la prima transizione viene dissolvenza dalla traccia 0 alla traccia 1, che è il comportamento predefinito. La seconda transizione passa dalla traccia 1 alla traccia 0. Si noti che entrambe le transizioni si trovano sulla traccia 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con i DirectShow di modifica](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transizioni ed effetti](transitions-and-effects.md)
</dt> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



