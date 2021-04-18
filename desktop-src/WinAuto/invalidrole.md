---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297907"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Testo

Il valore int restituito da Get \_ accRole non è una costante Role valida, ovvero un sistema di ruoli IE \_\_\*

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala un ruolo MSAA non valido. Ad esempio, il metodo [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) restituisce un valore integer che non esegue il mapping a una costante del ruolo oggetto valida, ad esempio ListItem del sistema del ruolo \_ \_ .

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione perché gli elementi potrebbero essere identificati erroneamente dall'utente.

## <a name="possible-causes"></a>Possibili cause

Per l'elemento o per il relativo padre è impostato un ruolo MSAA in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Ruoli oggetto**](object-roles.md)
</dt> </dl>

 

 




