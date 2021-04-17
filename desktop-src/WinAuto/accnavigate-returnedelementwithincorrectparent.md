---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: '\_ReturnedElementWithIncorrectParent AccNavigate'
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104557694"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>\_ReturnedElementWithIncorrectParent AccNavigate

## <a name="text"></a>Testo

La chiamata a accNavigate ((Live Search), 0, NAVDIR \_ FIRSTCHILD) che ha restituito (x-Gadget:///gadget.html) ha restituito un elemento padre non corretto ( \[ null \] ) e non (ricerca in tempo reale)

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) viene chiamato sull'elemento figlio restituito da [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando le \_ costanti di navigazione NAVDIR FIRSTCHILD o NAVDIR \_ LastChild), l'elemento padre restituito non corrisponde all'elemento padre specificato nella chiamata **accNavigate** .

![esempio di implementazione MSAA non valida che restituisce un elemento padre non corretto.](images/accchecker-invalid-msaa-parent.png)

Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




