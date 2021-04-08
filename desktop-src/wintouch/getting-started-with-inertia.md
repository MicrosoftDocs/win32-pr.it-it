---
title: Inerzia
description: Questa sezione illustra l'inerzia per Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inerzia
- inerzia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044199"
---
# <a name="inertia"></a>Inerzia

Questa sezione illustra l'inerzia per Windows Touch.

L'API di inerzia inclusa in Windows 7 consente un comportamento coerente degli oggetti nelle applicazioni Windows Touch fornendo un semplice modello di fisica. L'inerzia è abilitata usando il processore di inerzia, una classe che incapsula la funzionalità. Il processore di inerzia funziona elaborando gli eventi che vengono passati al termine delle manipolazioni degli oggetti e gestendo le traiettorie degli oggetti in modo coerente con altre applicazioni. Si noti che il processore di inerzia è strettamente associato al processore di manipolazione per semplificare l'aggiunta del supporto dell'inerzia alle applicazioni che usano le manipolazioni. Infatti, il processore di inerzia genera gli stessi eventi che il processore di manipolazione esegue. La sezione seguente illustra come iniziare a usare l'inerzia.



| Sezione                                                                      | Descrizione                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Meccanismi di inerzia](inertia-mechanics.md)                                   | Illustra le nozioni di base sui calcoli di inerzia.                                                                             |
| [Gestione dell'inerzia nel codice non gestito](handling-inertia-in-unmanaged-code.md) | Viene illustrato come utilizzare l'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) per la gestione dell'inerzia nel codice non gestito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifiche e inerzia](manipulation-and-inertia.md)
</dt> </dl>

 

 




