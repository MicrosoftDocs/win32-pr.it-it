---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221441"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Testo

La variante restituita da {0} deve essere un oggetto {1} , ma è un oggetto {2} .

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala uno stato MSAA non valido. Ad esempio, il metodo [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) usato per recuperare lo stato MSAA di un elemento deve restituire un valore integer che rappresenta una delle costanti di stato MSAA, ma restituisce invece un'altra variante.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché uno stato dell'elemento errato potrebbe essere segnalato all'utente.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo padre hanno uno stato MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Costanti di stato dell'oggetto**](object-state-constants.md)
</dt> </dl>

 

 




