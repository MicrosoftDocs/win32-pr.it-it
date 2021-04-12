---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85756504520f7d665c1cd1ba7db7c76c1ec5b12a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330172"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Testo

AccessibleObjectFromPoint ( {0} , {1} ) restituito {2} e previsto S \_ OK

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) non ha restituito S \_ OK come previsto per le coordinate specificate.

## <a name="possible-causes"></a>Possibili cause

-   Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.
-   Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




