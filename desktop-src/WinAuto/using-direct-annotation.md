---
title: Uso dell'annotazione diretta
description: Uso dell'annotazione diretta
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f0bdea5af896329b6836d21ca1dcee25bc2739
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338175"
---
# <a name="using-direct-annotation"></a><span data-ttu-id="903b3-103">Uso dell'annotazione diretta</span><span class="sxs-lookup"><span data-stu-id="903b3-103">Using Direct Annotation</span></span>

<span data-ttu-id="903b3-104">**Per utilizzare l'annotazione diretta per eseguire l'override del valore di una proprietà**</span><span class="sxs-lookup"><span data-stu-id="903b3-104">**To use direct annotation to override the value of a property**</span></span>

1.  <span data-ttu-id="903b3-105">Utilizzare la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) per creare l'oggetto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="903b3-105">Use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) function to create the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) object.</span></span>
2.  <span data-ttu-id="903b3-106">Chiamare [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passando **HWND**, ID oggetto, ID figlio, la proprietà di cui eseguire l'override e una [variante](/windows/win32/api/oaidl/ns-oaidl-variant) che contiene il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="903b3-106">Call [**IAccPropServices::SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passing the **HWND**, object ID, child ID, the property to be overridden, and a [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) containing the new value of the property.</span></span> <span data-ttu-id="903b3-107">Questo passaggio annota il valore.</span><span class="sxs-lookup"><span data-stu-id="903b3-107">This step annotates the value.</span></span>
3.  <span data-ttu-id="903b3-108">Rilasciare i puntatori all'interfaccia e liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="903b3-108">Release the interface pointers and free memory.</span></span>

<span data-ttu-id="903b3-109">Nell'esempio seguente viene illustrato come annotare la proprietà [**Role**](role-property.md) di un controllo testo statico.</span><span class="sxs-lookup"><span data-stu-id="903b3-109">The following example shows how to annotate the [**Role**](role-property.md) property of a static text control.</span></span>


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a><span data-ttu-id="903b3-110">Proprietà supportate quando si specifica un valore</span><span class="sxs-lookup"><span data-stu-id="903b3-110">Properties Supported When Specifying a Value</span></span>

<span data-ttu-id="903b3-111">Le seguenti proprietà di Microsoft Active Accessibility possono essere annotate quando si specifica un valore (il cui valore deve essere del tipo indicato) per l'annotazione diretta.</span><span class="sxs-lookup"><span data-stu-id="903b3-111">The following Microsoft Active Accessibility properties can be annotated when specifying a value (where the value must be of the noted type) for direct annotation.</span></span> <span data-ttu-id="903b3-112">Per eseguire l'override o aggiungere una proprietà di automazione interfaccia utente Microsoft a un controllo, è possibile specificare l'ID della proprietà di automazione interfaccia utente anziché l'ID della proprietà Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="903b3-112">To override or add a Microsoft UI Automation property to a control, you can specify the UI Automation property ID instead of the Microsoft Active Accessibility property ID.</span></span> <span data-ttu-id="903b3-113">Per un elenco di ID di automazione interfaccia utente, vedere [identificatori di proprietà](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="903b3-113">For a list of UI Automation IDs, see [Property Identifiers](uiauto-entry-propids.md).</span></span>



| <span data-ttu-id="903b3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="903b3-114">Property</span></span>                      | <span data-ttu-id="903b3-115">Type</span><span class="sxs-lookup"><span data-stu-id="903b3-115">Type</span></span>     |
|-------------------------------|----------|
| <span data-ttu-id="903b3-116">\_nome ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-116">PROPID\_ACC\_NAME</span></span>             | <span data-ttu-id="903b3-117">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-117">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-118">\_Descrizione ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-118">PROPID\_ACC\_DESCRIPTION</span></span>      | <span data-ttu-id="903b3-119">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-119">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-120">\_ruolo ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-120">PROPID\_ACC\_ROLE</span></span>             | <span data-ttu-id="903b3-121">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="903b3-121">VT\_I4</span></span>   |
| <span data-ttu-id="903b3-122">\_stato ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-122">PROPID\_ACC\_STATE</span></span>            | <span data-ttu-id="903b3-123">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="903b3-123">VT\_I4</span></span>   |
| <span data-ttu-id="903b3-124">Guida di PROPID \_ ACC \_</span><span class="sxs-lookup"><span data-stu-id="903b3-124">PROPID\_ACC\_HELP</span></span>             | <span data-ttu-id="903b3-125">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-125">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-126">\_KEYBOARDSHORTCUT ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-126">PROPID\_ACC\_KEYBOARDSHORTCUT</span></span> | <span data-ttu-id="903b3-127">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-127">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-128">\_DefaultAction propid ACC \_</span><span class="sxs-lookup"><span data-stu-id="903b3-128">PROPID\_ACC\_DEFAULTACTION</span></span>    | <span data-ttu-id="903b3-129">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-129">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-130">\_VALUEMAP ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-130">PROPID\_ACC\_VALUEMAP</span></span>         | <span data-ttu-id="903b3-131">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-131">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-132">\_ROLEMAP ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-132">PROPID\_ACC\_ROLEMAP</span></span>          | <span data-ttu-id="903b3-133">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-133">VT\_BSTR</span></span> |
| <span data-ttu-id="903b3-134">\_STATEMAP ACC \_ propid</span><span class="sxs-lookup"><span data-stu-id="903b3-134">PROPID\_ACC\_STATEMAP</span></span>         | <span data-ttu-id="903b3-135">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="903b3-135">VT\_BSTR</span></span> |



 

 

 