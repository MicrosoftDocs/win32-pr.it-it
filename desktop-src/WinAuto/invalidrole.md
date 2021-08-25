---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860001"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Testo

L'int restituito da get \_ accRole non è una costante di ruolo valida, ad esempio ROLE \_ SYSTEM\_\*

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento segnala un ruolo MSAA non valido. Ad esempio, il [**metodo get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) restituisce un valore intero che non esegue il mapping a una costante di ruolo oggetto valida, ad esempio ROLE \_ SYSTEM \_ LISTITEM.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione, perché gli elementi potrebbero essere erroneamente identificati per l'utente.

## <a name="possible-causes"></a>Possibili cause

L'elemento o il relativo elemento padre ha un ruolo MSAA impostato in modo non appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Ruoli degli oggetti**](object-roles.md)
</dt> </dl>

 

 




