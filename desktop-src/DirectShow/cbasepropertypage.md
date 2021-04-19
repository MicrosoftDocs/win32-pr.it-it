---
description: La classe CBasePropertyPage è una classe astratta per l'implementazione di una pagina delle proprietà. Utilizzare questa classe se si sta scrivendo un filtro (o un altro oggetto) che supporta le pagine delle proprietà.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Classe CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330310"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="6255e-104">Classe CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="6255e-104">CBasePropertyPage class</span></span>

![gerarchia di classi cbasepropertypage](images/cprop01.png)

<span data-ttu-id="6255e-106">La `CBasePropertyPage` classe è una classe astratta per l'implementazione di una pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="6255e-107">Utilizzare questa classe se si sta scrivendo un filtro (o un altro oggetto) che supporta le pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="6255e-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="6255e-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="6255e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6255e-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6255e-110">**\_bDirty m**</span><span class="sxs-lookup"><span data-stu-id="6255e-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="6255e-111">Indica se una o più proprietà sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="6255e-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="6255e-112">**\_DialogId m**</span><span class="sxs-lookup"><span data-stu-id="6255e-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="6255e-113">Identificatore di risorsa per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="6255e-114">**m \_ DLG**</span><span class="sxs-lookup"><span data-stu-id="6255e-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="6255e-115">Handle per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="6255e-116">**\_HWND m**</span><span class="sxs-lookup"><span data-stu-id="6255e-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="6255e-117">Handle per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="6255e-118">**\_pPageSite m**</span><span class="sxs-lookup"><span data-stu-id="6255e-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="6255e-119">Puntatore all'interfaccia **IPropertyPageSite** del sito della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="6255e-120">**\_IDQualifica m**</span><span class="sxs-lookup"><span data-stu-id="6255e-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="6255e-121">Identificatore di risorsa per una stringa che contiene il titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="6255e-122">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="6255e-122">Public Methods</span></span>                                                         | <span data-ttu-id="6255e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6255e-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="6255e-124">**CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="6255e-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="6255e-125">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6255e-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="6255e-126">**~ CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="6255e-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="6255e-127">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="6255e-127">Destructor method.</span></span> <span data-ttu-id="6255e-128">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="6255e-129">**OnActivate**</span><span class="sxs-lookup"><span data-stu-id="6255e-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="6255e-130">Chiamato quando la pagina delle proprietà viene attivata.</span><span class="sxs-lookup"><span data-stu-id="6255e-130">Called when the property page is activated.</span></span> <span data-ttu-id="6255e-131">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="6255e-132">**OnApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="6255e-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="6255e-133">Chiamato quando l'utente applica le modifiche alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="6255e-134">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="6255e-135">**OnConnect**</span><span class="sxs-lookup"><span data-stu-id="6255e-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="6255e-136">Fornisce un puntatore **IUnknown** all'oggetto associato alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="6255e-137">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="6255e-138">**OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="6255e-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="6255e-139">Chiamato quando viene eliminata definitivamente la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="6255e-140">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="6255e-141">**OnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="6255e-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="6255e-142">Chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato.</span><span class="sxs-lookup"><span data-stu-id="6255e-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="6255e-143">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="6255e-144">**OnReceiveMessage**</span><span class="sxs-lookup"><span data-stu-id="6255e-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="6255e-145">Chiamato quando la finestra di dialogo riceve un messaggio.</span><span class="sxs-lookup"><span data-stu-id="6255e-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="6255e-146">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="6255e-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="6255e-147">Metodi IPropertyPage</span><span class="sxs-lookup"><span data-stu-id="6255e-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="6255e-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6255e-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="6255e-149">**Activate**</span><span class="sxs-lookup"><span data-stu-id="6255e-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="6255e-150">Crea la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="6255e-151">**Applica**</span><span class="sxs-lookup"><span data-stu-id="6255e-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="6255e-152">Applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="6255e-153">**Disattivare**</span><span class="sxs-lookup"><span data-stu-id="6255e-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="6255e-154">Elimina definitivamente la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="6255e-155">**GetPageInfo**</span><span class="sxs-lookup"><span data-stu-id="6255e-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="6255e-156">Recupera le informazioni sulla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="6255e-157">**Help**</span><span class="sxs-lookup"><span data-stu-id="6255e-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="6255e-158">Richiama la guida della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="6255e-159">**IsPageDirty**</span><span class="sxs-lookup"><span data-stu-id="6255e-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="6255e-160">Indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a **IPropertyPage:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="6255e-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="6255e-161">**Spostare**</span><span class="sxs-lookup"><span data-stu-id="6255e-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="6255e-162">Posiziona e ridimensiona la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="6255e-163">**SetObjects**</span><span class="sxs-lookup"><span data-stu-id="6255e-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="6255e-164">Fornisce i puntatori **IUnknown** per gli oggetti associati alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="6255e-165">**SetPageSite**</span><span class="sxs-lookup"><span data-stu-id="6255e-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="6255e-166">Inizializza la pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="6255e-167">**Visualizza**</span><span class="sxs-lookup"><span data-stu-id="6255e-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="6255e-168">Consente di visualizzare o nascondere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="6255e-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="6255e-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="6255e-170">Indica alla pagina delle proprietà di elaborare una sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="6255e-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="6255e-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="6255e-171">Remarks</span></span>

<span data-ttu-id="6255e-172">Una pagina delle proprietà è un oggetto COM, pertanto è necessario generare un GUID per l'identificatore di classe (CLSID) e fornire una voce nella matrice [**CFactoryTemplate**](cfactorytemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="6255e-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="6255e-173">Per ulteriori informazioni, vedere [DirectShow e com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="6255e-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="6255e-174">Nell'esempio seguente viene illustrata una voce di class factory tipica:</span><span class="sxs-lookup"><span data-stu-id="6255e-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="6255e-175">Il filtro deve esporre l'interfaccia **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="6255e-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="6255e-176">Questa interfaccia contiene un solo metodo, **GetPages**, che restituisce il CLSID della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="6255e-177">Nell'esempio seguente viene illustrato come implementare questo metodo:</span><span class="sxs-lookup"><span data-stu-id="6255e-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="6255e-178">Ricordarsi di eseguire l'override anche del metodo **NonDelegatingQueryInterface** del filtro.</span><span class="sxs-lookup"><span data-stu-id="6255e-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="6255e-179">Per ulteriori informazioni, vedere [DirectShow e com](directshow-and-com.md) e [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6255e-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="6255e-180">Successivamente, creare la finestra di dialogo come risorsa nel progetto e creare una risorsa di stringa che contenga il titolo della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6255e-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="6255e-181">Entrambi gli ID risorsa sono parametri per il costruttore **CBasePropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="6255e-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="6255e-182">Mantenere la stringa del titolo in una risorsa rende più semplice la localizzazione della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6255e-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="6255e-183">La classe **CBasePropertyPage** fornisce un Framework per l'interfaccia **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="6255e-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="6255e-184">Questo framework chiama diversi metodi virtuali, tra cui [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md)e così via.</span><span class="sxs-lookup"><span data-stu-id="6255e-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="6255e-185">Nella classe di base, questi metodi restituiscono semplicemente S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6255e-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="6255e-186">La classe derivata dovrà eseguire l'override di alcuni o di tutti questi metodi virtuali.</span><span class="sxs-lookup"><span data-stu-id="6255e-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="6255e-187">Per informazioni dettagliate, vedere la sezione Osservazioni per i singoli metodi.</span><span class="sxs-lookup"><span data-stu-id="6255e-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="6255e-188">Per un esempio esteso di come usare questa classe per creare una pagina delle proprietà, vedere [creazione di una pagina delle proprietà di filtro](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="6255e-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6255e-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6255e-189">Requirements</span></span>



| <span data-ttu-id="6255e-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="6255e-190">Requirement</span></span> | <span data-ttu-id="6255e-191">Valore</span><span class="sxs-lookup"><span data-stu-id="6255e-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6255e-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6255e-192">Header</span></span><br/>  | <dl> <span data-ttu-id="6255e-193"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6255e-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6255e-194">Libreria</span><span class="sxs-lookup"><span data-stu-id="6255e-194">Library</span></span><br/> | <dl> <span data-ttu-id="6255e-195"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6255e-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




