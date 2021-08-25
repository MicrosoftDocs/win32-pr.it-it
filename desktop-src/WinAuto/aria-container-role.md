---
title: Errore del ruolo contenitore ARIA
description: Errore del ruolo contenitore ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507f094a5f7270565de0426b50afd6aef699607d857ef1ba7ed3d6c8bb1a1a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759831"
---
# <a name="aria-container-role-error"></a>Errore del ruolo contenitore ARIA

## <a name="text"></a>Testo

L'elemento con il discendente attivo definito non ha un ruolo contenitore **(casella** **combinata,** **griglia,** casella di riepilogo,  **menu,** **barra dei menu,** gruppo di **opzioni,** **albero,** **griglia** ad albero, **elenco** schede, **riga).**

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con **l'attributo aria-activedescendant.**

Un elemento sembra essere un contenitore con l'attributo **aria-activedescendant** impostato, ma l'attributo role dell'elemento non ha un valore valido per un contenitore.

Per correggere l'errore, impostare l'attributo role su un valore del ruolo WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications) valido per un elemento contenitore: **casella combinata,** **griglia,** casella di riepilogo,  **menu,** barra dei **menu,** **radiogroup,** **tablist,** **albero** o griglia **ad albero.** 

## <a name="example"></a>Esempio


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errore del ruolo ARIA](aria-role-invalid.md)
</dt> </dl>

 

 




