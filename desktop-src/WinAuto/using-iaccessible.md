---
title: Uso dell'interfaccia IAccessible
description: L'interfaccia IAccessible è una raccolta di metodi che espongono gli attributi e i comportamenti più comuni di un'ampia gamma di elementi dell'interfaccia utente.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c683e83928db53894c7c2c22976a5cf58c402c241e698dca5248230b1b24177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744896"
---
# <a name="using-the-iaccessible-interface"></a>Uso dell'interfaccia IAccessible

[**L'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è una raccolta di metodi che espongono gli attributi e i comportamenti più comuni di un'ampia gamma di elementi dell'interfaccia utente. Un elemento dell'interfaccia utente è un controllo, ad esempio un menu o un pulsante di invio, che fa parte dell'interfaccia utente. Un oggetto accessibile è un elemento dell'interfaccia utente con **un'interfaccia IAccessible** significativa.

Alcune delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) non sono applicabili a ogni tipo di elemento dell'interfaccia utente. Inoltre, l'implementazione **di IAccessible** varia da applicazione a applicazione.

Anche se i parametri e i valori restituiti per le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sono completamente specificati, il modo in cui un client deve usare una proprietà o come un server deve implementare una proprietà è talvolta soggetto a interpretazione.

In questa sezione vengono forniti suggerimenti, linee guida ed esempi per consentire alle applicazioni client di ottenere informazioni sugli elementi dell'interfaccia utente e per consentire alle applicazioni server di fornire informazioni appropriate.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Contenuto delle proprietà descrittive](content-of-descriptive-properties.md)
-   [Metodi e proprietà di selezione e stato attivo](selection-and-focus-properties-and-methods.md)
-   [Proprietà e metodi di navigazione degli oggetti](object-navigation-properties-and-methods.md)

 

 




