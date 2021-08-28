---
title: Errore della struttura della griglia ARIA
description: Errore della struttura della griglia ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b91010417ed01f211859839ceab124b299b10679b3d460f860c03e5b2473f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122381"
---
# <a name="aria-grid-structure-error"></a>Errore della struttura della griglia ARIA

## <a name="text"></a>Testo

L'elemento **con il ruolo** griglia non ha una struttura della griglia corrispondente o un markup accessibile.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi personalizzati con **l'attributo role** impostato su "grid". Non si applica ai tag di tabella HTML con ruolo **implicito** "grid".

Un elemento con  l'attributo del ruolo impostato su "grid" deve avere la struttura definita dal ruolo della griglia Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA), incluso il nome accessibile per la griglia e i relativi sottoelementi di intestazione.

Per correggere questo errore, esaminare l'implementazione per assicurarsi che sia conforme alla specifica WAI-ARIA. In particolare, assicurarsi che la struttura soddisfi le regole seguenti.

-   **la griglia** contiene **elementi riga** **o rowgroup.**
-   **rowgroup contiene** **elementi di** riga.
-   **Gli elementi** row contengono **elementi columnheader,** **gridcell** **o rowheader.**

È necessario definire un nome accessibile per gli elementi **grid**, **columnheader**, **gridcell** e **rowheader** usando uno degli attributi seguenti.

-   [**Attributo aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) per fare riferimento all'elemento contenente testo.
-   [**Attributo aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) per impostare direttamente il nome accessibile.
-   [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) per la creazione di una descrizione comando che viene usata contemporaneamente come nome.

 

 




