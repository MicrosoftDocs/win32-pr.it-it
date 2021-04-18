---
title: Esposizione di controlli in base ai controlli di sistema
description: Esposizione di controlli in base ai controlli di sistema
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399487"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="1afb3-103">Esposizione di controlli in base ai controlli di sistema</span><span class="sxs-lookup"><span data-stu-id="1afb3-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="1afb3-104">È consigliabile prendere in considerazione l'uso di una forma di annotazione dinamica, ovvero diretta, mappa di valori o server, prima di provare la tecnica descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="1afb3-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="1afb3-105">Per altre informazioni, vedere [API di annotazione dinamica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="1afb3-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="1afb3-106">Nella maggior parte dei casi, Microsoft Active Accessibility espone informazioni sui controlli sottoclassati o sottoclassati.</span><span class="sxs-lookup"><span data-stu-id="1afb3-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="1afb3-107">La superclasse e la creazione di sottoclassi consentono a uno sviluppatore di applicazioni di creare un controllo personalizzato con la funzionalità di base di un controllo del sistema e includere i miglioramenti forniti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1afb3-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="1afb3-108">Un controllo con superclasse ha un nome di classe di finestra diverso dal controllo del sistema su cui si basa.</span><span class="sxs-lookup"><span data-stu-id="1afb3-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="1afb3-109">Un controllo sottoclassato ha lo stesso nome della classe di finestra.</span><span class="sxs-lookup"><span data-stu-id="1afb3-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="1afb3-110">Per ulteriori informazioni sulla superclasse e la creazione di sottoclassi, vedere la documentazione di Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1afb3-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="1afb3-111">Poiché Microsoft Active Accessibility espone informazioni sui controlli forniti dal sistema, Microsoft Active Accessibility espone il controllo modificato a meno che un controllo sottoclassato o sottoclassato sia significativamente diverso dal controllo di base.</span><span class="sxs-lookup"><span data-stu-id="1afb3-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="1afb3-112">Per determinare se il controllo modificato è accessibile, gli sviluppatori di applicazioni devono utilizzare utilità quali [ispezione](inspect-objects.md) e [monitoraggio eventi accessibile](accessible-event-watcher.md) per confrontare il comportamento del controllo modificato con il controllo di base.</span><span class="sxs-lookup"><span data-stu-id="1afb3-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="1afb3-113">Se dopo l'utilizzo di queste utilità si stabilisce che il controllo modificato non è accessibile, è necessario considerare il controllo come qualsiasi altro controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1afb3-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="1afb3-114">Il controllo deve attivare gli eventi e la routine della finestra dell'applicazione deve rispondere al messaggio [**WM \_ GetObject**](wm-getobject.md)fornendo un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizzata dalle applicazioni client per ottenere informazioni sul controllo.</span><span class="sxs-lookup"><span data-stu-id="1afb3-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="1afb3-115">CreateStdAccessibleProxy e CreateStdAccessibleObject</span><span class="sxs-lookup"><span data-stu-id="1afb3-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="1afb3-116">Se tutte o la maggior parte delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo modificato sono le stesse del controllo di base, utilizzare [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) o [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) per semplificare l'implementazione dell'interfaccia **IAccessible** del controllo.</span><span class="sxs-lookup"><span data-stu-id="1afb3-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="1afb3-117">Quando si esegue la superclasse o si crea una sottoclasse di un controllo accessibile, tenere presente che l'oggetto recuperato dalla funzione [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) può implementare solo l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="1afb3-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="1afb3-118">Potrebbe includere altre interfacce, ad esempio [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span><span class="sxs-lookup"><span data-stu-id="1afb3-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="1afb3-119">Potrebbe essere necessario eseguire il wrapping di queste interfacce aggiuntive per mantenere il supporto per l'accessibilità fornito dalla implementazione originale del controllo.</span><span class="sxs-lookup"><span data-stu-id="1afb3-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="1afb3-120">Le funzioni [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) e [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) recuperano un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per il controllo di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="1afb3-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="1afb3-121">La differenza in queste funzioni è che **CreateStdAccessibleObject** usa il nome della classe di finestra ottenuto dal parametro *HWND* , mentre **CreateStdAccessibleProxy** usa il nome della classe di finestra specificato nel parametro *szClassName* .</span><span class="sxs-lookup"><span data-stu-id="1afb3-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="1afb3-122">Se pertanto si decide di usare queste funzioni, usare **CreateStdAccessibleProxy** per esporre le informazioni sui controlli con superclasse e una funzione con controlli sottoclassati.</span><span class="sxs-lookup"><span data-stu-id="1afb3-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="1afb3-123">Dopo avere ottenuto un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) al controllo di sistema, utilizzare il puntatore nell'implementazione dell'interfaccia **IAccessible** per il controllo modificato.</span><span class="sxs-lookup"><span data-stu-id="1afb3-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="1afb3-124">Se una proprietà o un metodo per il controllo modificato corrisponde al controllo di base, utilizzare il puntatore **IAccessible** per restituire le informazioni fornite dal controllo di base.</span><span class="sxs-lookup"><span data-stu-id="1afb3-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="1afb3-125">Se una proprietà per il controllo modificato è diversa dal controllo di base, eseguire l'override della proprietà del controllo di base.</span><span class="sxs-lookup"><span data-stu-id="1afb3-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="1afb3-126">Nell'esempio seguente **CAccCustomButton** è la classe definita dall'applicazione derivata da [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="1afb3-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="1afb3-127">La variabile membro **m \_ pAccDefaultButton** è un puntatore a un'interfaccia **IAccessible** che è stata recuperata da [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) durante la procedura di inizializzazione per il controllo.</span><span class="sxs-lookup"><span data-stu-id="1afb3-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="1afb3-128">In questo esempio, la proprietà **Role** per il controllo personalizzato corrisponde alla proprietà **Role** del controllo di sistema, pertanto viene restituita la proprietà **Role** del controllo di base.</span><span class="sxs-lookup"><span data-stu-id="1afb3-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="1afb3-129">Tuttavia, la proprietà **Description** è diversa da quella del controllo di base, quindi questa proprietà viene sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="1afb3-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="1afb3-130">Per ulteriori informazioni sulle proprietà e sui metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dei controlli di sistema, vedere [Appendice A: riferimenti agli elementi dell'interfaccia utente supportati](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1afb3-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 