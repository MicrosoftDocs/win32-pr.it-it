---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829371"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Testo

L'elemento è un oggetto IAccessible orfano nell'albero

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.

Questo problema è un problema per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento, perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.

## <a name="possible-causes"></a>Possibili cause

-   L'interazione dell'utente durante la verifica, ad esempio lo spostamento dello stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.
-   Implementazione di MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




