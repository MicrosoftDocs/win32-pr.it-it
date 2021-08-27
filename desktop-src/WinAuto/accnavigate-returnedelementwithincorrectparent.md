---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd040cda80e9dcb19543c8ee5134271693546dfdb8af76053b5a281340080765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122467"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Testo

La chiamata di accNavigate((Live Search), 0, NAVDIR FIRSTCHILD) che ha restituito (x-gadget:///gadget.html) ha restituito l'elemento padre non corretto( NULL ) e \_ \[ non \] (Ricerca live)

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Quando viene chiamato [**\_ get accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) sull'elemento figlio restituito da [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (usando le costanti di navigazione NAVDIR FIRSTCHILD o NAVDIR LASTCHILD), l'elemento padre restituito non corrisponde all'elemento padre specificato nella chiamata \_ \_ **accNavigate.**

![Esempio di implementazione msaa non valida che restituisce un elemento padre non corretto.](images/accchecker-invalid-msaa-parent.png)

Questo problema può causare problemi di navigazione per gli strumenti automatizzati perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




