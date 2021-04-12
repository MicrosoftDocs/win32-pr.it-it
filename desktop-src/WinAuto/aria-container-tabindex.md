---
title: Errore TabIndex del contenitore ARIA
description: Errore TabIndex del contenitore ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396714"
---
# <a name="aria-container-tabindex-error"></a>Errore TabIndex del contenitore ARIA

## <a name="text"></a>Testo

L'elemento è un contenitore focalizzabile con discendenti attivi definiti, ma senza valore **TabIndex** maggiore o uguale a 0.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si verifica per gli elementi che hanno l'attributo **aria-activedescendant** , non sono disabilitati e l'attributo **TabIndex** non è impostato su un valore maggiore o uguale a 0. Questi elementi devono essere in ordine di tabulazione perché sono responsabili della gestione degli eventi di tastiera per i relativi elementi figlio.

Per correggere l'errore, impostare l'attributo **TabIndex** su un valore maggiore o uguale a 0.

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

[Errore TabIndex del ruolo contenitore ARIA (senza discendente attivo)](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




