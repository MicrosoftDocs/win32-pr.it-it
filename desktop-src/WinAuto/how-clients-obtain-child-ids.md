---
title: Come i client ottengono gli ID figlio
description: Come i client ottengono gli ID figlio
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727722"
---
# <a name="how-clients-obtain-child-ids"></a>Come i client ottengono gli ID figlio

Gli sviluppatori client possono ottenere l'ID figlio di un oggetto nei modi seguenti:

-   Chiamare [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Questa funzione recupera una matrice di strutture [**Variant**](variant-structure.md) .
-   Eseguire una query sull'oggetto per verificare se supporta l'interfaccia [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . Se è presente, utilizzare [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) per ottenere gli ID figlio.
-   Raccogliere gli ID figlio chiamando il metodo [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) dell'oggetto padre.

> [!Note]  
> È responsabilità del client liberare la memoria usata per le strutture [**Variant**](variant-structure.md) . I client devono inoltre chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su qualsiasi interfaccia [**IDispatch**](idispatch-interface.md) restituita.

 

 

 