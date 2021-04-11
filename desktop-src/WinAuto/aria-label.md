---
title: Errore dell'etichetta ARIA
description: Errore dell'etichetta ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047530"
---
# <a name="aria-label-error"></a><span data-ttu-id="079fc-104">Errore dell'etichetta ARIA</span><span class="sxs-lookup"><span data-stu-id="079fc-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="079fc-105">Testo</span><span class="sxs-lookup"><span data-stu-id="079fc-105">Text</span></span>

<span data-ttu-id="079fc-106">L'elemento è di tipo **input**, **Button**, **Image-Button** o **Landmark** ma non ha un nome accessibile.</span><span class="sxs-lookup"><span data-stu-id="079fc-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="079fc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="079fc-107">Type</span></span>

<span data-ttu-id="079fc-108">Errore</span><span class="sxs-lookup"><span data-stu-id="079fc-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="079fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="079fc-109">Description</span></span>

<span data-ttu-id="079fc-110">Questo errore si applica a:</span><span class="sxs-lookup"><span data-stu-id="079fc-110">This error applies to:</span></span>

-   <span data-ttu-id="079fc-111">Campi di input del modulo:</span><span class="sxs-lookup"><span data-stu-id="079fc-111">Form input fields:</span></span>
    -   <span data-ttu-id="079fc-112">Tag HTML-**tipo di input \[ = " \| password \| del testo casella di controllo \| \| \| posta elettronica file di \| \| colore Tel data DateTime \| \| \| -ora locale- \| URL di ricerca dell'intervallo di numeri del \| \| mese \| \| \| \| " \]**, **Select**, **DataList** e **textarea**.</span><span class="sxs-lookup"><span data-stu-id="079fc-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="079fc-113">WAI-ARIA Roles:**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **Radio**, **TextBox**, **Tree**, **Slider** e **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="079fc-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="079fc-114">Pulsanti immagini/immagine/pulsanti</span><span class="sxs-lookup"><span data-stu-id="079fc-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="079fc-115">Tag HTML:**IMG**, **input \[ Type = "Image \| Button" \]** e **Button**.</span><span class="sxs-lookup"><span data-stu-id="079fc-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="079fc-116">Ruoli WAI-ARIA:**IMG** e **Button**.</span><span class="sxs-lookup"><span data-stu-id="079fc-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="079fc-117">Punti di riferimento</span><span class="sxs-lookup"><span data-stu-id="079fc-117">Landmarks</span></span>
    -   <span data-ttu-id="079fc-118">WAI-ARIA Roles:**Region**, **banner**, **complementari**, **ContentInfo**, **form**, **Main**, **Navigation** e **Search**.</span><span class="sxs-lookup"><span data-stu-id="079fc-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="079fc-119">AccChecker Mostra questo errore anche per gli elementi per i quali il nome accessibile è impostato per impostazione predefinita in base al contenuto HTML interno (vedere l'elemento **banner** nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="079fc-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="079fc-120">In questi casi, è possibile disattivare questi errori.</span><span class="sxs-lookup"><span data-stu-id="079fc-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="079fc-121">Tutti gli elementi dell'interfaccia utente semanticamente importanti, ad esempio i campi del form (ad esempio **input**, **SELECT**, **textarea**), le immagini, i pulsanti e i punti di riferimento (tag che rappresentano le aree logiche), devono avere il nome accessibile per consentire agli utilità per la lettura dello schermo di annunciarli correttamente.</span><span class="sxs-lookup"><span data-stu-id="079fc-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="079fc-122">Per correggere l'errore, impostare il nome accessibile in uno dei modi seguenti (elencati nell'ordine di preferenza).</span><span class="sxs-lookup"><span data-stu-id="079fc-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="079fc-123">Campi modulo: usare il tag **Label** e impostare l'attributo **for** sul valore **ID** del campo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="079fc-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="079fc-124">Pulsante immagine/immagine: impostare l'attributo **ALT** .</span><span class="sxs-lookup"><span data-stu-id="079fc-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="079fc-125">Buttons: impostare il testo della didascalia del pulsante.</span><span class="sxs-lookup"><span data-stu-id="079fc-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="079fc-126">Per qualsiasi elemento:</span><span class="sxs-lookup"><span data-stu-id="079fc-126">For any element:</span></span>
    -   <span data-ttu-id="079fc-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo: impostare sul valore **ID** dell'elemento contenente la stringa del nome accessibile.</span><span class="sxs-lookup"><span data-stu-id="079fc-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="079fc-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: impostare sulla stringa del nome accessibile.</span><span class="sxs-lookup"><span data-stu-id="079fc-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="079fc-129">attributo [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : impostare sulla stringa del nome accessibile (creare anche una **Descrizione comando**).</span><span class="sxs-lookup"><span data-stu-id="079fc-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="079fc-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="079fc-130">Example</span></span>


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




