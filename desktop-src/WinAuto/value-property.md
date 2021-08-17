---
title: Proprietà Value
description: La proprietà Value fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto . Non tutti gli oggetti supportano la proprietà Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcebf689016add11008b5d8249ce4eaa8adf4a99a406afea8d1267f01f94201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133274"
---
# <a name="value-property"></a>Proprietà Value

La **proprietà Value** fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto . Non tutti gli oggetti supportano **la proprietà** Value.

La **proprietà Value** viene recuperata chiamando [**IAccessible::get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

La **proprietà Value** indica al client le informazioni visive contenute in un oggetto . Ad esempio, il valore di un controllo di modifica è il testo che contiene, mentre una voce di menu non ha alcun valore.

## <a name="providing-hierarchical-information"></a>Fornire informazioni gerarchiche

La **proprietà Value** fornisce informazioni gerarchiche nei casi in cui, ad esempio, un controllo visualizzazione albero. Anche se l'oggetto padre nel controllo visualizzazione albero non fornisce informazioni nella proprietà **Value,** ogni elemento all'interno del controllo ha un valore in base zero che rappresenta il relativo livello all'interno della gerarchia. Gli elementi di primo livello hanno un valore pari a zero, gli elementi di secondo livello hanno un valore pari a uno e così via.

 

 




