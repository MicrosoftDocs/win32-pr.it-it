---
title: Errore della tabella di presentazione ARIA
description: Errore della tabella di presentazione ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896c7ec4061119535ed544cfc41598c1387d98011eb275f6a0345d9334a7dc9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122286"
---
# <a name="aria-presentation-table-error"></a>Errore della tabella di presentazione ARIA

## <a name="text"></a>Testo

La tabella usata per il layout non deve avere informazioni di intestazione, nome accessibile o riepilogo definite (**th**, **summary**, **aria-describedby**, **aria-labelledby,** **aria-label**, **title**, **caption** attributes).

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica ai tag di tabella HTML con l'attributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) impostato su "presentation" o con una tabella con una singola cella (tabella 1×1).

Questo errore indica che una tabella è contrassegnata solo come layout (ha ), ma contiene anche informazioni di accessibilità come se fosse una tabella di dati, che può generare confusione per gli utenti dell'utilità per la lettura `role="presentation"` dello schermo.

Per risolvere questo errore, determinare se la tabella è effettivamente solo una tabella di layout e, in tal caso, rimuovere il markup accessibile:

-   [**Elemento CAPTION,**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) [**attributi aria-labelledby,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title.**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title)
-   [**attributi summary**](https://www.bing.com/search?q=**summary**) [**o aria-describedby.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)
-   [**Tag THEAD.**](https://developer.mozilla.org/docs/Web/HTML/Element/thead)

## <a name="example"></a>Esempio

![html per un elemento table, con attributi come summary che attivano l'errore della tabella di presentazione aria come markup HTML ](images/aria-layout-table.png)

## <a name="remarks"></a>Commenti

Se si determina che una tabella richiede informazioni sull'accessibilità, rimuovere l'attributo [**del**](https://developer.mozilla.org/docs/Web/HTML/Reference) ruolo o impostarlo su un valore diverso da "presentation".

 

 




