---
title: Proprietà Value
description: La proprietà Value fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto. Non tutti gli oggetti supportano la proprietà Value.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330223"
---
# <a name="value-property"></a>Proprietà Value

La proprietà **value** fornisce una rappresentazione testuale delle informazioni visive contenute in un oggetto. Non tutti gli oggetti supportano la proprietà **value** .

La proprietà **value** viene recuperata chiamando [**IAccessible:: Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).

La proprietà **value** indica al client le informazioni visive contenute in un oggetto. Ad esempio, il valore di un controllo di modifica è il testo che contiene, mentre una voce di menu non contiene alcun valore.

## <a name="providing-hierarchical-information"></a>Fornire informazioni gerarchiche

La proprietà **value** fornisce informazioni gerarchiche nei casi, ad esempio un controllo di visualizzazione ad albero. Sebbene l'oggetto padre nel controllo di visualizzazione albero non fornisca informazioni nella proprietà **value** , ogni elemento all'interno del controllo ha un valore in base zero che rappresenta il livello all'interno della gerarchia. Gli elementi di primo livello hanno un valore pari a zero, gli elementi di secondo livello hanno un valore pari a uno e così via.

 

 




