---
title: Errore tabindex del ruolo del contenitore ARIA (senza discendente attivo)
description: Errore tabindex del ruolo del contenitore ARIA (senza discendente attivo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994341"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Errore tabindex del ruolo del contenitore ARIA (senza discendente attivo)

## <a name="text"></a>Testo

L'elemento è un contenitore attivabile senza un discendente attivo definito, ma nessun elemento figlio ha **tabindex** maggiore o uguale a 0.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati. Questi elementi implementano la navigazione tramite tastiera tra gli elementi figlio usando il concetto noto come *roving index*. In questo concetto, gli **attributi tabindex** degli elementi figlio vengono mantenuti dinamicamente, assicurando che un solo elemento figlio sia sempre in ordine di tabulazione.

Per correggere l'errore, impostare **l'attributo tabindex** di uno degli elementi figlio su un valore uguale o maggiore di 0.

## <a name="example"></a>Esempio


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore tabindex del contenitore ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




