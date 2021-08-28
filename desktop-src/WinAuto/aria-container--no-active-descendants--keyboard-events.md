---
title: Errore di accessibilità della tastiera per il ruolo contenitore ARIA (senza discendente attivo)
description: Errore di accessibilità della tastiera per il ruolo contenitore ARIA (senza discendente attivo)
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b653ac3bf2dc8254b25c52a89cdb3503b89b9f05997a3ea9fb4f4ef3a77cb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071881"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Errore di accessibilità della tastiera per il ruolo contenitore ARIA (senza discendente attivo)

## <a name="text"></a>Testo

L'elemento è un contenitore attivabile senza discendenti attivi definiti e senza gestori eventi / **OnKeyDown OnKeyPress** / **OnKeyUp** (né nel contenitore né in uno degli elementi figlio).

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi che hanno un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati. Questi elementi implementano la navigazione tramite tastiera tra gli elementi figlio usando il concetto noto come *indice di approvazione.* In questo concetto, gli **attributi tabindex** degli elementi figlio vengono mantenuti in modo dinamico, assicurando che in qualsiasi momento un solo elemento figlio sia in ordine di tabulazione.

Questo errore indica che un elemento contenitore che non dispone dell'attributo **aria-activedescendant** e che non è disabilitato non è accessibile agli utenti della tastiera. Il problema esiste perché il contenitore non ha i gestori eventi della tastiera necessari (**keydown,** **keyup** o **keypress**) e nessuno degli elementi figlio del contenitore.

Per correggere l'errore, definire un gestore eventi **keydown,** **keyup** o **keypress** per il contenitore o uno dei relativi elementi figlio.

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

[Errore di accessibilità della tastiera del ruolo contenitore ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




