---
title: Navigazione gerarchica
description: Spesso i client devono spostarsi tra gli oggetti in base alle relazioni padre-figlio. Ad esempio, un client potrebbe avere già informazioni su un controllo della barra degli strumenti, ma non avere informazioni sui pulsanti in esso contenuti.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221409"
---
# <a name="hierarchical-navigation"></a>Navigazione gerarchica

Spesso i client devono spostarsi tra gli oggetti in base alle relazioni padre-figlio. Ad esempio, un client potrebbe avere già informazioni su un controllo della barra degli strumenti, ma non avere informazioni sui pulsanti in esso contenuti.

L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) espone le relazioni gerarchiche tra gli oggetti. I client possono passare da un oggetto padre ai relativi elementi figlio o da un oggetto figlio al relativo padre chiamando [**IAccessible:: Get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) o [**IAccessible:: Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




