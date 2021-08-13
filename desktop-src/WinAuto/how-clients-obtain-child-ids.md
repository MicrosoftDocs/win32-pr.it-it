---
title: Come i client ottengono gli ID figlio
description: Come i client ottengono gli ID figlio
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388601"
---
# <a name="how-clients-obtain-child-ids"></a>Come i client ottengono gli ID figlio

Gli sviluppatori client possono ottenere l'ID figlio di un oggetto nei modi seguenti:

-   Chiamare [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Questa funzione recupera una matrice di [**strutture VARIANT.**](variant-structure.md)
-   Eseguire una query sull'oggetto per verificare se supporta [**l'interfaccia IEnumVARIANT.**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) Se è presente, usare [**IEnumVARIANT::Next per**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) ottenere gli ID figlio.
-   Raccogliere gli ID figlio chiamando il metodo [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) dell'oggetto padre.

> [!Note]  
> È responsabilità del client liberare la memoria usata per le [**strutture VARIANT.**](variant-structure.md) I client devono anche chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su qualsiasi [**interfaccia IDispatch**](idispatch-interface.md) restituita.

 

 

 