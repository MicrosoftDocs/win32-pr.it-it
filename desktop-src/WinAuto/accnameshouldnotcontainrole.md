---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f09bd9ccdf27c5f52a45466b6b8145cfe23248cc175777f57202aac6530791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899731"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Testo

Il nome dell'elemento ( {0} ) non deve contenere il testo del ruolo dell'elemento ( {1} )

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

Il nome di un elemento incorpora il ruolo MSAA o il tipo di controllo dell'interfaccia utente. Ad esempio, questo avviso può verificarsi se il metodo [**get \_ accName,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) usato per recuperare il nome MSAA di un elemento, restituisce "ROLE \_ SYSTEM \_ \_ SCROLLBAR". \*

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento, perché il ruolo verrà letto due volte o potrebbe essere imprevedibile o non intuitivo per gli utenti.

## <a name="possible-causes"></a>Possibili cause

-   All'elemento o al relativo elemento padre è assegnato un nome o un'etichetta non corretta.
-   L'elemento o il relativo elemento padre ha un nome predefinito che non è stato modificato in un nome descrittivo. Ad esempio, button1.
-   Uno sviluppatore non è a conoscenza del fatto che le utilità per la lettura dello schermo leggono i nomi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




