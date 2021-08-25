---
title: Errore di accessibilità della tastiera del ruolo contenitore ARIA
description: Errore di accessibilità della tastiera del ruolo contenitore ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591098ba6e38836f1f39d13e72495bc1d7a3d5f9fe088873661e3dd3a7e65d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122401"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Errore di accessibilità della tastiera del ruolo contenitore ARIA

## <a name="text"></a>Testo

L'elemento è un contenitore con funzionalità del mouse discendente attivo e personalizzato, ma senza la corrispondente funzionalità della tastiera: gestori eventi JavaScript per **OnKeyDown** o **OnKeyPress.**

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con **l'attributo aria-activedescendant.** Questi elementi dispongono di uno o più gestori eventi del mouse **(mousemove,** **mousedown** o **mouseup),** ma mancano i gestori eventi della tastiera equivalenti (**keydown,** **keyup** o **keypress).** I gestori eventi della tastiera sono necessari per garantire che l'utente possa richiamare la funzionalità dell'elemento usando la tastiera e per garantire che l'elemento mantenga **l'attributo aria-activedescendant.**

Per correggere l'errore, implementare uno dei gestori eventi della tastiera.

## <a name="example"></a>Esempio


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore di accessibilità della tastiera per il ruolo contenitore ARIA (senza discendente attivo)](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




