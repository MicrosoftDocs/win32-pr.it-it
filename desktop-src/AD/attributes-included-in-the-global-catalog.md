---
title: Inclusione di attributi nel catalogo globale
description: Il catalogo globale di una foresta include una replica parziale di ogni oggetto della foresta.
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- Attributi inclusi nel catalogo globale AD
- Attributi AD, inclusi nel catalogo globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472702"
---
# <a name="including-attributes-in-the-global-catalog"></a>Inclusione di attributi nel catalogo globale

Il catalogo globale di una foresta include una replica parziale di ogni oggetto della foresta. Per ogni oggetto, il catalogo globale include solo un subset di tutti gli attributi dell'oggetto. L'attributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) di un oggetto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) è impostato su **true** se l'attributo viene replicato nel catalogo globale.

Gli attributi con le seguenti caratteristiche sono appropriati per l'archiviazione nel catalogo globale:

-   L'attributo è interessante a livello globale, perché l'attributo è necessario per individuare gli oggetti che possono essere presenti in qualsiasi punto della foresta o perché l'accesso in lettura all'attributo è utile anche quando l'oggetto completo non è accessibile. Un esempio del primo tipo è l'attributo [**location**](/windows/desktop/ADSchema/a-location) , che può essere usato per trovare un oggetto [**PrintQueue**](/windows/desktop/ADSchema/c-printqueue) . Un esempio del secondo tipo è [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber), perché è possibile chiamare un utente anche se non è possibile accedere a una replica completa del relativo oggetto [**utente**](/windows/desktop/ADSchema/c-user) .
-   La volatilità dell'attributo è molto bassa. Si tratta di un aspetto importante, perché se una classe Attribute è inclusa nel catalogo globale, le modifiche apportate a ogni valore della classe Attribute nell'intera foresta aziendale vengono replicate in tutti i server di catalogo globale nell'organizzazione.
-   Le dimensioni del valore dell'attributo sono ridotte. "Small" è molto soggettiva: quando si posiziona un attributo nel catalogo globale, si consideri l'impatto della replica dell'attributo a tutti i server di catalogo globale nell'organizzazione. Minore è l'attributo, minore è l'effetto. Poiché la replica si verifica solo quando l'attributo viene modificato, anche l'effetto della replica è inferiore, in quanto la volatilità diminuisce, quindi un attributo di grandi dimensioni con una volatilità molto bassa potrebbe avere un effetto complessivo inferiore rispetto a un attributo di piccole dimensioni con volatilità elevata.

Quando si decide se collocare o meno un attributo nel catalogo globale, tenere presente che si sta negoziando una maggiore replica e un maggiore spazio di archiviazione su disco nei server di catalogo globale per prestazioni di query, potenzialmente più veloci. In genere, è possibile utilizzare il catalogo globale per cercare un oggetto di interesse, in modo da poter leggere gli attributi selezionati dell'oggetto. Se gli attributi a cui si è interessati vengono replicati nel catalogo globale, è possibile leggerli direttamente dal catalogo globale. In alternativa, per leggere gli attributi che non vengono replicati nel catalogo globale, è necessario eseguire passaggi aggiuntivi per recuperarli. In questo caso, dopo la ricerca nel catalogo globale per trovare l'oggetto di interesse, è necessario leggere il nome distinto dell'oggetto dal catalogo globale, usare il DN per eseguire il binding direttamente a una replica completa dell'oggetto, che può trovarsi in un server diverso e infine leggere gli attributi non globali del catalogo dalla replica completa dell'oggetto.

Gli attributi sottoposti a query e a cui viene fatto riferimento, ad esempio il nome e il numero di telefono, sono utili per includere nel catalogo globale. Un attributo a cui si fa riferimento raramente, ad esempio "driverVersion", per le stampanti è più adatto al catalogo globale.

 

 