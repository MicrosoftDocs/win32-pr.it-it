---
title: Errore della tabella di presentazione ARIA
description: Errore della tabella di presentazione ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734586"
---
# <a name="aria-presentation-table-error"></a>Errore della tabella di presentazione ARIA

## <a name="text"></a>Testo

Per la tabella usata per il layout non devono essere definite intestazioni, nome accessibile o informazioni di riepilogo (**th**, **Summary**, **aria-describedby**, **aria-labelledby**, **aria-etichetta**, **titolo**, attributi **didascalia** ).

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica ai tag della tabella HTML con l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) impostato su "Presentation" o con una tabella con una sola cella (1 × 1 tabella).

Questo errore indica che una tabella è contrassegnata come solo layout (ha `role="presentation"` ), ma contiene anche informazioni sull'accessibilità come se si trattasse di una tabella di dati, che può essere confusa per gli utenti di lettura schermo.

Per risolvere questo errore, determinare se la tabella è effettivamente semplicemente una tabella di layout e, in caso affermativo, rimuovere il markup accessibile:

-   Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-etichetta**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**titolo**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributi.
-   attributi [**Summary**](https://www.bing.com/search?q=**summary**) o [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .
-   Tag [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .

## <a name="example"></a>Esempio

![HTML per un elemento Table, con attributi, ad esempio Riepilogo, che attivano l'errore della tabella di presentazione aria mostrata come markup HTML sottoposta a indisponibilità ](images/aria-layout-table.png)

## <a name="remarks"></a>Commenti

Se si determina che una tabella necessita di informazioni sull'accessibilità, rimuovere l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) o impostarlo su un valore diverso da "Presentation".

 

 




