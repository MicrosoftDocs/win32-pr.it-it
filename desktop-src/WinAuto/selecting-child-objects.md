---
title: Selezione di oggetti figlio
description: I client chiamano il metodo IAccessible accSelect per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio di un oggetto. Le costanti SELFLAG specificate con la chiamata definiscono l'operazione da eseguire.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328911"
---
# <a name="selecting-child-objects"></a>Selezione di oggetti figlio

I client chiamano il metodo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per modificare la selezione o lo stato attivo della tastiera tra gli elementi figlio di un oggetto. Le [costanti SELFLAG](selflag.md) specificate con la chiamata definiscono l'operazione da eseguire.

Se [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) viene chiamato con il flag [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto figlio con **HWND**, il flag viene applicato solo se l'elemento padre dell'oggetto ha lo stato attivo.

## <a name="performing-complex-selection-operations"></a>Esecuzione di operazioni di selezione complesse

Di seguito vengono descritti i valori SELFLAG da specificare quando si chiama [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) per eseguire operazioni di selezione complesse.

**Per simulare un clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**Per selezionare un elemento di destinazione simulando CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**Per annullare la selezione di un elemento di destinazione simulando CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**Per simulare MAIUSC + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**Per selezionare un intervallo di oggetti e impostare lo stato attivo sull'ultimo oggetto**

1.  Specificare [**SELFLAG \_ TAKEFOCUS**](selflag.md) nell'oggetto iniziale per impostare l'ancoraggio di selezione.
2.  Chiamare di nuovo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) sull'ultimo oggetto.

**Per deselezionare tutti gli oggetti**

1.  Specificare [**SELFLAG \_ TAKESELECTION**](selflag.md) in qualsiasi oggetto. Questo flag deseleziona tutti gli oggetti selezionati eccetto quello appena selezionato.
2.  Chiamare di nuovo [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) e specificare [**SELFLAG \_ REMOVESELECTION**](selflag.md) nell'oggetto rimanente.

 

 




