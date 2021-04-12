---
title: Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)
description: Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221464"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)

## <a name="text"></a>Testo

L'elemento è un contenitore attivabile senza un discendente attivo definito, ma nessun elemento figlio ha un **TabIndex** maggiore o uguale a 0.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si verifica per gli elementi che hanno un ruolo contenitore, non hanno un attributo **aria-activedescendant** e non sono disabilitati. Questi elementi implementano la navigazione da tastiera tra gli elementi figlio utilizzando il concetto noto come *Indice itinerante*. In questo concetto, gli attributi **TabIndex** degli elementi figlio vengono mantenuti in modo dinamico, assicurando che in ogni momento un solo elemento figlio sia in ordine di tabulazione.

Per correggere l'errore, impostare l'attributo **TabIndex** di uno degli elementi figlio su un valore maggiore o uguale a 0.

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

[Errore TabIndex del contenitore ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




