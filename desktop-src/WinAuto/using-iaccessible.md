---
title: Utilizzo dell'interfaccia IAccessible
description: L'interfaccia IAccessible è una raccolta di metodi che espongono gli attributi e i comportamenti più comuni di un'ampia gamma di elementi dell'interfaccia utente.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330428"
---
# <a name="using-the-iaccessible-interface"></a>Utilizzo dell'interfaccia IAccessible

L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è una raccolta di metodi che espongono gli attributi e i comportamenti più comuni di un'ampia gamma di elementi dell'interfaccia utente. Un elemento dell'interfaccia utente è un controllo, ad esempio un menu o un pulsante di push, che fa parte dell'interfaccia utente. Un oggetto accessibile è un elemento dell'interfaccia utente che dispone di un'interfaccia **IAccessible** significativa.

Alcune proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) non sono applicabili a ogni tipo di elemento dell'interfaccia utente. Inoltre, l'implementazione di **IAccessible** varia a seconda dell'applicazione.

Sebbene i parametri e i valori restituiti per le proprietà e i metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siano specificati in modo completo, il modo in cui un client deve utilizzare una proprietà o il modo in cui un server deve implementare una proprietà è talvolta soggetto a interpretazione.

In questa sezione vengono forniti suggerimenti, linee guida ed esempi per aiutare le applicazioni client a ottenere informazioni sugli elementi dell'interfaccia utente e per aiutare le applicazioni server a fornire le informazioni appropriate.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Contenuto delle proprietà descrittive](content-of-descriptive-properties.md)
-   [Proprietà e metodi di selezione e messa a fuoco](selection-and-focus-properties-and-methods.md)
-   [Proprietà e metodi di navigazione degli oggetti](object-navigation-properties-and-methods.md)

 

 




