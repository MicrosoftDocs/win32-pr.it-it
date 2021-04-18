---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298961"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Testo

L'elemento è un oggetto IAccessible orfano nell'albero

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'indirizzo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.

Questo problema rappresenta un problema per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.

## <a name="possible-causes"></a>Possibili cause

-   Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.
-   Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Navigazione tramite hit testing e posizione dello schermo](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




