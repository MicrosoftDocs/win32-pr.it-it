---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644737"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Testo

Chiamare a accNavigate((Fare clic su Snooze per ricordarlo di nuovo in:), 1, NAVDIR NEXT), quindi \_ accNavigate((Open), 2, NAVDIR PREVIOUS), dovrebbe aver restituito Click Snooze to be reminded again \_ in:(ChildId=1), but returned Click Snooze to be reminded again in:

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

l'uso di [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per attraversare l'albero degli elementi della destinazione di verifica non restituisce lo stesso elemento iniziale quando la direzione dell'attraversamento viene inversa.

![esempio di un'implementazione msaa non valida che ha causato una navigazione round trip non corretta](images/accchecker-invalid-round-trip.png)

Questo problema può causare problemi di navigazione per gli strumenti automatizzati perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




