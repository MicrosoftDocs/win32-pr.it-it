---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221801"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Testo

Chiamata a accNavigate ((fare clic su Snooze per ricordarsi di nuovo in:), 1, NAVDIR \_ successivo), quindi accNavigate ((Open), 2, NAVDIR \_ precedente), dovrebbe avere restituito clic su Snooze per ricordarsi di nuovo in: (childID = 1), ma restituito fare clic su Snooze per ricordarlo di nuovo in:

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

l'uso di [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per attraversare l'albero degli elementi della destinazione di verifica non restituisce lo stesso elemento iniziale quando la direzione di attraversamento è invertita.

![esempio di implementazione MSAA non valida che ha causato una navigazione non corretta del round trip](images/accchecker-invalid-round-trip.png)

Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




