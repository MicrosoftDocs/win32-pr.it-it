---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708728"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Testo

Un controllo ha stati/proprietà che sono incoerenti {0} e {1}

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala stati MSAA incoerenti o in conflitto o proprietà di automazione interfaccia utente. Ad esempio, quando il metodo [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) restituisce una delle combinazioni seguenti.

-   \_Sistema \_ di stato espanso e \_ sistema di stato \_ compresso
-   \_Sistema \_ di stato selezionato e non stato \_ sistema \_ selezionabile
-   \_Sistema \_ di stato con stato attivo e non \_ attivabile dal sistema di stato \_

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché uno stato dell'elemento errato potrebbe essere segnalato all'utente.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo padre hanno uno stato MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Costanti di stato dell'oggetto**](object-state-constants.md)
</dt> <dt>

[Stati e proprietà](uiauto-msaa.md)
</dt> </dl>

 

 




