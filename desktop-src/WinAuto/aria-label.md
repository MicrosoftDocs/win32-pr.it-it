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
# <a name="aria-label-error"></a>Errore dell'etichetta ARIA

## <a name="text"></a>Testo

L'elemento è di tipo **input**, **Button**, **Image-Button** o **Landmark** ma non ha un nome accessibile.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a:

-   Campi di input del modulo:
    -   Tag HTML-**tipo di input \[ = " \| password \| del testo casella di controllo \| \| \| posta elettronica file di \| \| colore Tel data DateTime \| \| \| -ora locale- \| URL di ricerca dell'intervallo di numeri del \| \| mese \| \| \| \| " \]**, **Select**, **DataList** e **textarea**.
    -   WAI-ARIA Roles:**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **Radio**, **TextBox**, **Tree**, **Slider** e **SpinButton**.
-   Pulsanti immagini/immagine/pulsanti
    -   Tag HTML:**IMG**, **input \[ Type = "Image \| Button" \]** e **Button**.
    -   Ruoli WAI-ARIA:**IMG** e **Button**.
-   Punti di riferimento
    -   WAI-ARIA Roles:**Region**, **banner**, **complementari**, **ContentInfo**, **form**, **Main**, **Navigation** e **Search**.

> [!Note]  
> AccChecker Mostra questo errore anche per gli elementi per i quali il nome accessibile è impostato per impostazione predefinita in base al contenuto HTML interno (vedere l'elemento **banner** nell'esempio precedente). In questi casi, è possibile disattivare questi errori.

 

Tutti gli elementi dell'interfaccia utente semanticamente importanti, ad esempio i campi del form (ad esempio **input**, **SELECT**, **textarea**), le immagini, i pulsanti e i punti di riferimento (tag che rappresentano le aree logiche), devono avere il nome accessibile per consentire agli utilità per la lettura dello schermo di annunciarli correttamente.

Per correggere l'errore, impostare il nome accessibile in uno dei modi seguenti (elencati nell'ordine di preferenza).

-   Campi modulo: usare il tag **Label** e impostare l'attributo **for** sul valore **ID** del campo di destinazione.
-   Pulsante immagine/immagine: impostare l'attributo **ALT** .
-   Buttons: impostare il testo della didascalia del pulsante.
-   Per qualsiasi elemento:
    -   [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo: impostare sul valore **ID** dell'elemento contenente la stringa del nome accessibile.
    -   [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: impostare sulla stringa del nome accessibile.
    -   attributo [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : impostare sulla stringa del nome accessibile (creare anche una **Descrizione comando**).

## <a name="example"></a>Esempio


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



 

 




