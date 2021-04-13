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
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="53275-103">Utilizzo dell'interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="53275-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="53275-104">L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è una raccolta di metodi che espongono gli attributi e i comportamenti più comuni di un'ampia gamma di elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="53275-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="53275-105">Un elemento dell'interfaccia utente è un controllo, ad esempio un menu o un pulsante di push, che fa parte dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="53275-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="53275-106">Un oggetto accessibile è un elemento dell'interfaccia utente che dispone di un'interfaccia **IAccessible** significativa.</span><span class="sxs-lookup"><span data-stu-id="53275-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="53275-107">Alcune proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) non sono applicabili a ogni tipo di elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="53275-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="53275-108">Inoltre, l'implementazione di **IAccessible** varia a seconda dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53275-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="53275-109">Sebbene i parametri e i valori restituiti per le proprietà e i metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siano specificati in modo completo, il modo in cui un client deve utilizzare una proprietà o il modo in cui un server deve implementare una proprietà è talvolta soggetto a interpretazione.</span><span class="sxs-lookup"><span data-stu-id="53275-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="53275-110">In questa sezione vengono forniti suggerimenti, linee guida ed esempi per aiutare le applicazioni client a ottenere informazioni sugli elementi dell'interfaccia utente e per aiutare le applicazioni server a fornire le informazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="53275-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53275-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="53275-111">In this section</span></span>

-   [<span data-ttu-id="53275-112">Contenuto delle proprietà descrittive</span><span class="sxs-lookup"><span data-stu-id="53275-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="53275-113">Proprietà e metodi di selezione e messa a fuoco</span><span class="sxs-lookup"><span data-stu-id="53275-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="53275-114">Proprietà e metodi di navigazione degli oggetti</span><span class="sxs-lookup"><span data-stu-id="53275-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




