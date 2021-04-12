---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396955"
---
# <a name="elementisnotchildofelementsparent"></a>ElementIsNotChildOfElementsParent

## <a name="text"></a>Testo

L'elemento non è un elemento figlio del padre

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) viene chiamato sull'elemento figlio restituito da [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando le \_ costanti di navigazione NAVDIR FIRSTCHILD o NAVDIR \_ LastChild), l'elemento padre restituito non corrisponde all'elemento padre specificato nella chiamata **accNavigate** .

Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




