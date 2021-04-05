---
title: Errore del ruolo del contenitore ARIA
description: Errore del ruolo del contenitore ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955778"
---
# <a name="aria-container-role-error"></a>Errore del ruolo del contenitore ARIA

## <a name="text"></a>Testo

L'elemento con un **discendente attivo** definito non dispone di un ruolo contenitore (**casella combinata**, **griglia**, **ListBox**, **menu**, **barra** dei menu, **radiogruppo**, **albero**, **Treegrid**, in **particolare**, **riga**).

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con l'attributo **aria-activedescendant** .

Un elemento sembra essere un contenitore in cui è impostato l'attributo **aria-activedescendant** , ma l'attributo Role dell'elemento non dispone di un valore valido per un contenitore.

Per correggere l'errore, impostare l'attributo **Role** su un valore del ruolo Web Accessibility Initiative (Wai-aria) accessibile da Internet, che è valido per un elemento contenitore: **ComboBox**, **Grid**, **ListBox**, **menu**, **barra** dei menu, **RadioGroup**, in **particolare**, **Tree** o **Treegrid**.

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

 

 




