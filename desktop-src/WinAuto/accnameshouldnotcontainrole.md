---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714194"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Testo

Il nome dell'elemento ( {0} ) non deve contenere il testo del ruolo dell'elemento ( {1} )

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

Il nome di un elemento incorpora il proprio ruolo MSAA o il tipo di controllo UIA. Ad esempio, questo avviso può verificarsi se il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , utilizzato per recuperare il nome MSAA di un elemento, restituisce "Role \_ System \_ ScrollBar \_ \* ".

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché il ruolo verrà letto due volte o potrebbe non essere pronunciabile o non intuitivo per gli utenti.

## <a name="possible-causes"></a>Possibili cause

-   All'elemento o al relativo padre è assegnato un nome o un'etichetta non corretta.
-   L'elemento o il relativo padre ha un nome predefinito che non è stato modificato in un nome descrittivo. Ad esempio, button1.
-   Uno sviluppatore non è in grado di leggere i nomi dei lettori dello schermo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




