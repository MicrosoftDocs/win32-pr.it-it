---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327687"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Testo

AccessibleObjectFromPoint( {0} , {1} ) restituito e previsto S {2} \_ OK

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) non ha restituito S \_ OK come previsto per le coordinate specificate.

## <a name="possible-causes"></a>Possibili cause

-   L'interazione dell'utente durante la verifica, ad esempio lo spostamento dello stato attivo su un HWND non di destinazione, ha interferito con il processo di verifica.
-   Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




