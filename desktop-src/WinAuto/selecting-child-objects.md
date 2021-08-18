---
title: Selezione di oggetti figlio
description: I client chiamano il metodo IAccessible accSelect per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio in un oggetto . Le costanti SELFLAG specificate con la chiamata definiscono l'operazione da eseguire.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc15ab48a42be44c62c8c7bc2b9151158875509a2e43010c5da70830b2f2973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133684"
---
# <a name="selecting-child-objects"></a>Selezione di oggetti figlio

I client chiamano il [**metodo IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio in un oggetto . Le [costanti SELFLAG specificate](selflag.md) con la chiamata definiscono l'operazione da eseguire.

Se [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) viene chiamato con il flag [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto figlio con **HWND,** il flag ha effetto solo se l'elemento padre dell'oggetto ha lo stato attivo.

## <a name="performing-complex-selection-operations"></a>Esecuzione di operazioni di selezione complesse

Di seguito vengono descritti i valori SELFLAG da specificare quando si chiama [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per eseguire operazioni di selezione complesse.

**Per simulare un clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**Per selezionare un elemento di destinazione simulando CTRL+clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**Per annullare la selezione di un elemento di destinazione simulando CTRL+clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**Per simulare MAIUSC+ clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**Per selezionare un intervallo di oggetti e spostare lo stato attivo sull'ultimo oggetto**

1.  Specificare [**SELFLAG \_ TAKEFOCUS sull'oggetto**](selflag.md) iniziale per impostare l'ancoraggio di selezione.
2.  Chiamare [**di nuovo IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) sull'ultimo oggetto.

**Per deselezionare tutti gli oggetti**

1.  Specificare [**SELFLAG \_ TAKESELECTION**](selflag.md) per qualsiasi oggetto. Questo flag deseleziona tutti gli oggetti selezionati tranne quello appena selezionato.
2.  Chiamare [**di nuovo IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ REMOVESELECTION**](selflag.md) per l'oggetto rimanente.

 

 




