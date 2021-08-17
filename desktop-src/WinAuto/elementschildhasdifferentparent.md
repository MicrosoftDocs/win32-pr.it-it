---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829186"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Testo

Child( ) {0} dell'elemento ha un elemento padre( {1} ) diverso dall'elemento

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore indica che, quando viene chiamato [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) sugli elementi figlio dell'elemento di destinazione, gli elementi figlio non segnalano un elemento padre coerente.

![un esempio degli elementi figlio di un elemento che segnala un elemento padre incoerente](images/accchecker-inconsistent-parent.png)

Questo problema può causare problemi di navigazione per gli strumenti automatizzati perché l'attraversamento di elementi potrebbe essere imprevedibile e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione di MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




