---
title: VariantNotInt (CheckRole)
description: VariantNotInt (CheckRole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330220"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole)

## <a name="text"></a>Testo

La variante restituita da {0} deve essere un oggetto {1} , ma è un oggetto {2} .

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala un ruolo MSAA non valido. Ad esempio, il metodo [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) usato per recuperare il ruolo MSAA di un elemento deve restituire un valore integer che rappresenta una delle costanti del ruolo MSAA, ma restituisce invece un'altra variante.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi potrebbero essere identificati erroneamente dall'utente.

## <a name="possible-causes"></a>Possibili cause

Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Ruoli oggetto**](object-roles.md)
</dt> </dl>

 

 




