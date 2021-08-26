---
title: Errore dell'etichetta ARIA
description: Errore dell'etichetta ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42abee9028db8c3a4070d9b60d0650187339fc4c9ec34d0b70f720c27e973897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122321"
---
# <a name="aria-label-error"></a>Errore dell'etichetta ARIA

## <a name="text"></a>Testo

L'elemento è di **tipo input**, **button**, **image-button** o **landmark,** ma non ha un nome accessibile.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a:

-   Campi di input del modulo:
    -   Tag HTML:**input \[ type= "text \| password checkbox radio file email tel color \| \| \| \| \| \| \| \| datetime \| datetime datetime-local \| time week week month number range search \| \| \| \| \| \| \] url"**, **select**, **datalist** e **textarea**.
    -   Ruoli WAI-ARIA:**casella** di **controllo,** **casella combinata,** casella di **riepilogo,** **radiogroup,** **radio,** **casella** di **testo,** albero, dispositivo di scorrimento e pulsante **di selezione.**
-   Pulsanti/pulsanti di immagini/immagini
    -   Tag HTML:**img,** **input \[ type="image \| button" \]** e **button**.
    -   Ruoli WAI-ARIA:**img** e **pulsante**.
-   Punti di riferimento
    -   Ruoli WAI-ARIA:**area**, **banner**, **complementare**, **contentinfo**, **form**, **main**, **navigation** e **search**.

> [!Note]  
> AccChecker mostra questo errore anche per gli elementi per cui il nome accessibile è impostato per impostazione predefinita in base al contenuto HTML interno (vedere l'elemento **banner** nell'esempio precedente). In questi casi, è possibile eliminare questi errori.

 

Tutti gli elementi dell'interfaccia utente semanticamente importanti, ad esempio i campi modulo (ad esempio **input**, **select**, **textarea),** immagini, pulsanti e punti di riferimento (tag che rappresentano aree logiche) devono avere il nome accessibile per consentire alle utilità per la lettura dello schermo di annunciarli correttamente.

Per correggere l'errore, impostare il nome accessibile in uno dei modi seguenti (elencati nell'ordine di preferenza).

-   Campi modulo: usare il tag **etichetta** e impostare **l'attributo for** sul **valore id** del campo di destinazione.
-   Pulsante Immagine/immagine: impostare **l'attributo alt.**
-   Pulsanti: impostare il testo della didascalia del pulsante.
-   Per qualsiasi elemento:
    -   [**Attributo aria-labelledby:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) impostato sul valore **id** dell'elemento contenente la stringa del nome accessibile.
    -   [**Attributo aria-label:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) impostato sulla stringa del nome accessibile.
    -   [**Attributo title:**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) impostare sulla stringa del nome accessibile (creare anche una **descrizione comando).**

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



 

 




