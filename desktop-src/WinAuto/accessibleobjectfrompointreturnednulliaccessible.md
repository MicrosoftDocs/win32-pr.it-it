---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71963ad564454dcb90266b4fe4c63ba7282dbc514ab286629798420ff1db9f6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327697"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Testo

AccessibleObjectFromPoint( {0} , ) ha {1} restituito Null

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'indirizzo dell'interfaccia [**IAccessible dell'elemento dell'interfaccia**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utente ottenuto per le coordinate specificate è NULL.

## <a name="possible-causes"></a>Possibili cause

-   L'interazione dell'utente durante la verifica, ad esempio lo spostamento dello stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.
-   Implementazione di MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




