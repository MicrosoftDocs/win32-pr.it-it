---
title: Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)
description: Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856118"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Errore di accessibilità della tastiera del ruolo contenitore ARIA (senza discendente attivo)

## <a name="text"></a>Testo

L'elemento è un contenitore attivabile senza un discendente attivo definito e senza **OnKeyDown** / **OnKeyPress** /  gestori eventi (né nel contenitore né in uno degli elementi figlio).

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si verifica per gli elementi che hanno un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati. Questi elementi implementano la navigazione da tastiera tra gli elementi figlio utilizzando il concetto noto come *Indice itinerante*. In questo concetto, gli attributi **TabIndex** degli elementi figlio vengono mantenuti in modo dinamico, assicurando che in ogni momento un solo elemento figlio sia in ordine di tabulazione.

Questo errore indica che un elemento contenitore che non dispone dell'attributo **aria-activedescendant** , e che non è disabilitato, non è accessibile agli utenti della tastiera. Il problema è dovuto al fatto che il contenitore non contiene i gestori eventi di tastiera necessari (**KeyDown**, **KeyUp** o **KeyPress**) e nessuno degli elementi figlio del contenitore.

Per correggere l'errore, definire un gestore eventi **KeyDown**, **KeyUp** o **KeyPress** per il contenitore o uno dei relativi elementi figlio.

## <a name="example"></a>Esempio


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore di accessibilità tastiera ruolo contenitore ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




