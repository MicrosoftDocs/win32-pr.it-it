---
title: Proprietà e metodi
description: Analogamente a qualsiasi oggetto OLE, un controllo offre la maggior parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701b100be635fdb8db9cb51f258dc722edd23eca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044381"
---
# <a name="properties-and-methods"></a><span data-ttu-id="0be12-103">Proprietà e metodi</span><span class="sxs-lookup"><span data-stu-id="0be12-103">Properties and Methods</span></span>

<span data-ttu-id="0be12-104">Analogamente a qualsiasi oggetto OLE, un controllo offre la maggior parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="0be12-104">Like any OLE object, a control provides much of its functionality through a set of incoming interfaces with properties and methods.</span></span>

<span data-ttu-id="0be12-105">Un controllo espone proprietà e metodi tramite l'automazione OLE, in modo che i contenitori possano accedervi sotto il controllo di un linguaggio di programmazione fornito dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="0be12-105">A control exposes properties and methods through OLE automation so that containers can access them under the control of a container-supplied programming language.</span></span>

<span data-ttu-id="0be12-106">Per supportare l'accesso alle proprietà tramite un'interfaccia utente, un controllo fornisce pagine di proprietà, il supporto per \_ le proprietà OLEIVERB, l'esplorazione delle proprietà e la data binding tramite la modifica della proprietà notifica.</span><span class="sxs-lookup"><span data-stu-id="0be12-106">To support access to properties through a user interface, a control provides property pages, support for OLEIVERB\_PROPERTIES, per property browsing, and data binding through property change notfications.</span></span>

-   <span data-ttu-id="0be12-107">Tramite le pagine delle proprietà, un controllo può visualizzarne le proprietà, indipendentemente dal relativo contenitore, se necessario.</span><span class="sxs-lookup"><span data-stu-id="0be12-107">Through property pages a control can display its properties, independent of its container, if necessary.</span></span>
-   <span data-ttu-id="0be12-108">Grazie al supporto \_ delle proprietà OLEIVERB, l'elemento Properties viene visualizzato nel menu del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0be12-108">By supporting OLEIVERB\_PROPERTIES, the Properties item is displayed on the container's menu.</span></span> <span data-ttu-id="0be12-109">Quindi, l'utente finale può selezionare l'elemento **Properties** per visualizzare le pagine delle proprietà del controllo e modificare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="0be12-109">Then, the end user can select the **Properties** item to view the control's property pages and modify the properties.</span></span>
-   <span data-ttu-id="0be12-110">Per esplorazione di proprietà è supportato un contenitore in grado di visualizzare le proprietà del controllo come parte di una finestra delle proprietà più ampia che può includere proprietà di diversi controlli nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="0be12-110">Per property browsing supports a container that can display the control's properties as part of a larger property sheet that may include properties from several controls in the container.</span></span>
-   <span data-ttu-id="0be12-111">Tramite la notifica delle modifiche alle proprietà, un controllo può notificare a un client che le relative proprietà sono state modificate, consentendo al client di eseguire le azioni necessarie di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="0be12-111">Through property change notification, a control can notify a client that its properties have change, allowing the client to take any necessary actions as a result.</span></span>

<span data-ttu-id="0be12-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="0be12-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0be12-113">Proprietà del controllo</span><span class="sxs-lookup"><span data-stu-id="0be12-113">Control Properties</span></span>](control-properties.md)
-   [<span data-ttu-id="0be12-114">Metodi di controllo</span><span class="sxs-lookup"><span data-stu-id="0be12-114">Control Methods</span></span>](control-methods.md)

## <a name="related-topics"></a><span data-ttu-id="0be12-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0be12-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be12-116">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="0be12-116">ActiveX Controls</span></span>](activex-controls.md)
</dt> <dt>

[<span data-ttu-id="0be12-117">Pagine delle proprietà e finestre delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0be12-117">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




