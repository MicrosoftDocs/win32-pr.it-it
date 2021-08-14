---
title: Errore DI ARIA Tabindex
description: Errore DI ARIA Tabindex
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1637008b6679f196f7bba0701606e0514abe44410032e1a5ffc063977ddf10e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326746"
---
# <a name="aria-tabindex-error"></a>Errore DI ARIA Tabindex

## <a name="text"></a>Testo

L'elemento non è disabilitato e ha un gestore dell'evento **click,** ma ha **tabIndex** < 0 e non è nell'ordine di tabulazione per impostazione predefinita.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi che hanno un gestore dell'evento Click e non sono disabilitati. Questi elementi devono essere nell'ordine di tabulazione. In questo modo si garantisce che un elemento possa essere raggiunto usando il tasto TAB, ovvero il modo in cui gli utenti dell'utilità per la lettura dello schermo in genere esplorano l'interfaccia utente.

Per correggere l'errore, impostare [**l'attributo tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) su un valore uguale o maggiore di 0. Non è necessario impostare in modo esplicito l'attributo **tabindex** per i tag nell'ordine di tabulazione per impostazione predefinita, ad esempio [**(con**](https://developer.mozilla.org/docs/Web/HTML/Element/a) l'attributo [**href),**](https://developer.mozilla.org/docs/Web/HTML/Attributes) [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (escluso "hidden"), [](https://developer.mozilla.org/docs/Web/HTML/Element/select)select , [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)e [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (come parte della mappa immagine).

## <a name="example"></a>Esempio


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




