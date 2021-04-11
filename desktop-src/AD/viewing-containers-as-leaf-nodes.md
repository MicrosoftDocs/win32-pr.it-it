---
title: Visualizzazione di contenitori come nodi foglia
description: Qualsiasi oggetto in Active Directory Domain Services può essere un contenitore di altri oggetti.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Visualizzazione di contenitori come nodi foglia
- contenitori AD, visualizzazione come nodi foglia
- AD foglia, visualizzazione di contenitori come nodi foglia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336759"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="83717-106">Visualizzazione di contenitori come nodi foglia</span><span class="sxs-lookup"><span data-stu-id="83717-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="83717-107">Qualsiasi oggetto in Active Directory Domain Services può essere un contenitore di altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="83717-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="83717-108">Questo può ingombrare l'interfaccia utente, pertanto è possibile dichiarare che un oggetto di una classe specifica deve essere visualizzato solo come foglia nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="83717-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="83717-109">L'attributo **treatAsLeaf** è un attributo di identificatore di visualizzazione a valore singolo che determina se gli oggetti di tale classe devono essere visualizzati solo come oggetti foglia.</span><span class="sxs-lookup"><span data-stu-id="83717-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="83717-110">Questo attributo è un valore booleano che, se **true**, indica che gli oggetti della classe devono essere visualizzati solo come elementi foglia.</span><span class="sxs-lookup"><span data-stu-id="83717-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="83717-111">Se **false**, indica che gli oggetti della classe possono essere visualizzati come contenitore o foglia.</span><span class="sxs-lookup"><span data-stu-id="83717-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="83717-112">Come tutti gli attributi dell'identificatore di visualizzazione, l'attributo **treatAsLeaf** viene impostato in base alle singole impostazioni locali, pertanto questo attributo può essere localizzato in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="83717-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="83717-113">Ad esempio, la **visualizzazione dell'utente** per l'identificatore di visualizzazione delle impostazioni locali inglesi (0409) ha l'attributo **TreatAsLeaf** impostato su **true** per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="83717-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="83717-114">In questo modo, l'interfaccia utente visualizzerà tutti gli oggetti **utente** come oggetti foglia.</span><span class="sxs-lookup"><span data-stu-id="83717-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="83717-115">\*\*Per impostare il valore dell'attributo \*\*treatAsLeaf\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83717-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="83717-116">Eseguire l'associazione all'attributo di visualizzazione desiderato nelle impostazioni locali desiderate.</span><span class="sxs-lookup"><span data-stu-id="83717-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="83717-117">Per ulteriori informazioni e un esempio di codice, vedere [contenitore DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="83717-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="83717-118">Usare il metodo [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) per impostare l'attributo **treatAsLeaf** su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="83717-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="83717-119">Per eseguire il commit delle modifiche nella directory, chiamare il metodo [**IADs:: seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="83717-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 