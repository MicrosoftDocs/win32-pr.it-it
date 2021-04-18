---
title: Metodi di proprietà dell'interfaccia
description: Molte interfacce ADSI sono progettate per supportare l'automazione e pertanto sono interfacce duali che supportano l'accesso client tramite le interfacce IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà dell'interfaccia
- ADSI ADSI, Reference, method Property Explained
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300452"
---
# <a name="interface-property-methods"></a><span data-ttu-id="76111-105">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="76111-105">Interface Property Methods</span></span>

<span data-ttu-id="76111-106">Molte interfacce ADSI sono progettate per supportare l'automazione e pertanto sono interfacce duali che supportano l'accesso client tramite le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="76111-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="76111-107">I client non di automazione, ad esempio quelli scritti in C/C++, risolvono direttamente la chiamata al metodo, usando il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e chiamano direttamente il metodo.</span><span class="sxs-lookup"><span data-stu-id="76111-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="76111-108">I client di automazione, noti anche come client associati al nome, ad esempio quelli scritti in Visual Basic o Visual Basic Scripting Edition (VBScript), devono risolvere indirettamente la chiamata al metodo usando il metodo [**Dispatch**](/previous-versions/windows/desktop/automat/dispinterface) .</span><span class="sxs-lookup"><span data-stu-id="76111-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="76111-109">Un'interfaccia ADSI che supporta l'automazione definisce i metodi di proprietà per il recupero e la modifica delle proprietà di un oggetto che implementa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="76111-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="76111-110">I metodi di proprietà hanno nomi con **Get** \_ e **put** \_ anteposti ai nomi di proprietà appropriati, ad esempio **get \_ User** e **put \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="76111-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="76111-111">Ogni **metodo \_ Get** accetta un solo parametro come output.</span><span class="sxs-lookup"><span data-stu-id="76111-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="76111-112">Questo parametro è un indirizzo allocato dal metodo di una variabile del tipo di dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="76111-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="76111-113">Alla restituzione, questa variabile presuppone il valore corrente della proprietà richiesta.</span><span class="sxs-lookup"><span data-stu-id="76111-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="76111-114">Il chiamante deve rilasciare la memoria allocata della variabile quando la proprietà non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="76111-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="76111-115">Ogni **metodo \_ put** accetta un solo parametro come input per il tipo di dati della proprietà corrispondente.</span><span class="sxs-lookup"><span data-stu-id="76111-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="76111-116">Il parametro include un nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="76111-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="76111-117">Nell'esempio di codice seguente viene illustrata la chiamata dei metodi di proprietà che seguono la routine consueta per chiamare la funzione membro di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="76111-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="76111-118">Nell'esempio di codice seguente viene illustrata la chiamata dei metodi di proprietà nei client di automazione, che possono essere leggermente diversi.</span><span class="sxs-lookup"><span data-stu-id="76111-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="76111-119">Ad esempio, Visual Basic usa la notazione del punto.</span><span class="sxs-lookup"><span data-stu-id="76111-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="76111-120">Tutti i parametri e i tipi restituiti devono essere di quelli definiti dal tipo di dati VARIANT.</span><span class="sxs-lookup"><span data-stu-id="76111-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="76111-121">Tutti i metodi su un'interfaccia doppia restituiscono un valore HRESULT per indicare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="76111-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="76111-122">Per ulteriori informazioni su come ottenere e impostare le proprietà sugli oggetti ADSI, vedere la pagina relativa alla [cache delle proprietà](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="76111-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 