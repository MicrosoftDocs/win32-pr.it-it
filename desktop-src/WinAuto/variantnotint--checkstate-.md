---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3334a3609e9d64c1bb7109cc6f5bb52a2d09f9f9ac18cc41abf5d761f8e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052169"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Testo

La variante restituita da {0} deve essere un oggetto , ma è un oggetto {1} {2} .

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala uno stato MSAA non valido. Ad esempio, il metodo [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usato per recuperare lo stato MSAA di un elemento deve restituire un valore intero che rappresenta una delle costanti di stato MSAA, ma restituisce invece un'altra variante.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento perché all'utente potrebbe essere segnalato uno stato di elemento non corretto.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo elemento padre ha uno stato MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Costanti di stato dell'oggetto**](object-state-constants.md)
</dt> </dl>

 

 




