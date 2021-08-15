---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfed0716423d8b1fef182be7cb0cb8ef122cf70cff6a574069fe40b63549f744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829550"
---
# <a name="elementischildofparentmulipletimes"></a>ElementIsChildOfParentMulipleTimes

## <a name="text"></a>Testo

L'elemento accParent dell'elemento è ( {0} ), ma l'elemento originale è un elemento {1} figlio

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando [**get \_ accParent viene**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) chiamato sull'elemento di destinazione, segnala di essere figlio dello stesso elemento padre più volte.

Questo problema può causare problemi di navigazione per gli strumenti automatizzati perché l'attraversamento di elementi potrebbe essere imprevedibile e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione di MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




