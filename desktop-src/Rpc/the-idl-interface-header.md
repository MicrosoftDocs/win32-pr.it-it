---
title: Intestazione dell'interfaccia IDL
description: L'intestazione dell'interfaccia IDL specifica le informazioni sull'interfaccia nel suo complesso. A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118391"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="63c03-104">Intestazione dell'interfaccia IDL</span><span class="sxs-lookup"><span data-stu-id="63c03-104">The IDL Interface Header</span></span>

<span data-ttu-id="63c03-105">L'intestazione dell'interfaccia IDL specifica le informazioni sull'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="63c03-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="63c03-106">A differenza di ACF, l'intestazione dell'interfaccia contiene attributi indipendenti dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="63c03-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="63c03-107">Gli attributi nell'intestazione dell'interfaccia sono globali per l'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63c03-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="63c03-108">Ovvero si applicano all'interfaccia e a tutte le relative parti.</span><span class="sxs-lookup"><span data-stu-id="63c03-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="63c03-109">Questi attributi sono racchiusi tra parentesi quadre all'inizio della definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63c03-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="63c03-110">Un esempio è illustrato nella definizione di interfaccia seguente:</span><span class="sxs-lookup"><span data-stu-id="63c03-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="63c03-111">Si noti che l'intestazione dell'interfaccia contiene gli **\[** attributi [**UUID**](/windows/desktop/Midl/uuid) **\]** e **\[** [**Version**](/windows/desktop/Midl/version) **\]** .</span><span class="sxs-lookup"><span data-stu-id="63c03-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="63c03-112">Poiché rappresentano rispettivamente l'UUID e il numero di versione dell'interfaccia, sono attributi dell'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63c03-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="63c03-113">Il corpo dell'interfaccia può contenere anche attributi.</span><span class="sxs-lookup"><span data-stu-id="63c03-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="63c03-114">Tuttavia, non sono applicabili all'intera interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63c03-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="63c03-115">Si riferiscono a elementi specifici nell'interfaccia, ad esempio i parametri di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="63c03-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="63c03-116">Per una descrizione completa degli attributi dell'intestazione IDL, vedere la Guida di [riferimento al linguaggio MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="63c03-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 