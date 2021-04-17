---
title: Errore di accessibilità tastiera ruolo contenitore ARIA
description: Errore di accessibilità tastiera ruolo contenitore ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330943"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Errore di accessibilità tastiera ruolo contenitore ARIA

## <a name="text"></a>Testo

L'elemento è un contenitore con funzionalità del mouse attive discendenti e personalizzate ma senza la corrispondente funzionalità della tastiera: gestori eventi JavaScript per **OnKeyDown** o **OnKeyPress**.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con l'attributo **aria-activedescendant** . Questi elementi hanno uno o più gestori di eventi del mouse (**MouseMove**, **MouseDown** o **MouseUp**), ma mancano i gestori eventi di tastiera equivalenti (**KeyDown**, **KeyUp** o **KeyPress**). I gestori degli eventi della tastiera sono necessari per garantire che l'utente possa richiamare la funzionalità dell'elemento tramite la tastiera e per assicurarsi che l'elemento mantenga l'attributo **aria-activedescendant** .

Per correggere l'errore, implementare uno dei gestori di eventi della tastiera.

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

[Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




