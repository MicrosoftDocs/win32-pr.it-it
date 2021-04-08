---
title: Errore struttura griglia ARIA
description: Errore struttura griglia ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734594"
---
# <a name="aria-grid-structure-error"></a>Errore struttura griglia ARIA

## <a name="text"></a>Testo

L'elemento con il ruolo **Grid** non dispone di una struttura di griglia o di un markup accessibile corrispondente.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi personalizzati per i quali l'attributo **Role** è impostato su "Grid". Non si applica ai tag di tabella HTML con **ruolo** implicito "Grid".

Un elemento il cui attributo **Role** è impostato su "Grid" deve avere la struttura definita dal ruolo Grid (Wai-aria) accessibile Web Accessibility Initiative, incluso il nome accessibile per la griglia e i relativi sottoelementi di intestazione.

Per correggere l'errore, esaminare l'implementazione per assicurarsi che sia conforme alla specifica WAI-ARIA. In particolare, assicurarsi che la struttura soddisfi le regole seguenti.

-   la **griglia** contiene elementi **Row** o **rowgroup** .
-   **rowgroup** contiene elementi **Row** .
-   gli elementi **Row** contengono elementi **ColumnHeader** o **GridCell** o **RowHeader** .

Per gli elementi **Grid**, **ColumnHeader**, **GridCell** e **RowHeader** è necessario definire un nome accessibile utilizzando uno degli attributi seguenti.

-   [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo per fare riferimento all'elemento contenente il testo.
-   [**aria-etichetta**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo per impostare direttamente il nome accessibile.
-   [**titolo**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) per la creazione di una descrizione comando che viene utilizzata allo stesso tempo come nome.

 

 




