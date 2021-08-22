---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30533125c342bd80134c9eab45f14917a3b3ad04af9d969140c49502cbfd192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644841"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Testo

Un controllo ha stati/proprietà incoerenti {0} e {1}

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala stati MSAA incoerenti o in conflitto o Automazione interfaccia utente proprietà. Ad esempio, quando il [**metodo get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) restituisce una delle combinazioni seguenti.

-   STATE \_ SYSTEM EXPANDED E STATE SYSTEM \_ \_ \_ COLLAPSED
-   STATE \_ SYSTEM SELECTED e non STATE SYSTEM \_ \_ \_ SELECTABLE
-   STATE \_ SYSTEM FOCUSED e non STATE SYSTEM \_ \_ \_ FOCUSABLE

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione perché all'utente potrebbe essere segnalato uno stato di elemento non corretto.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo elemento padre ha uno stato MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Costanti dello stato dell'oggetto**](object-state-constants.md)
</dt> <dt>

[Stati e proprietà](uiauto-msaa.md)
</dt> </dl>

 

 




