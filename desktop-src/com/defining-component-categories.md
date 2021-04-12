---
title: Definizione delle categorie di componenti
description: Definizione delle categorie di componenti
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222109"
---
# <a name="defining-component-categories"></a>Definizione delle categorie di componenti

L'autore della definizione di una categoria di componenti crea un GUID univoco (CATId) che viene pubblicato insieme alla definizione. Altre parti conoscono la definizione di questo tipo e possono utilizzare di conseguenza le classi supportate. Analogamente alla firma del metodo di un'interfaccia, la semantica di una categoria non deve essere modificata dopo l'installazione. È preferibile mantenere la compatibilità con le versioni precedenti della categoria introducendo un nuovo identificatore di categoria con la semantica modificata.

Poiché gli identificatori di interfaccia (IID) e gli identificatori di categoria di componenti (CATId) si trovano in spazi dei nomi diversi, sembra che sia possibile usare lo stesso GUID sia per un IID che per un CATId. Tuttavia, poiché IID vengono spesso utilizzati per il CLSID del server proxy/stub dell'interfaccia, è possibile che si verifichi un conflitto. Pertanto, non utilizzare lo stesso GUID per un IID e un CATId.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Gestione categorie di componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




