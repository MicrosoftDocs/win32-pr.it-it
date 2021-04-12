---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332660"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Testo

Elemento senza nome

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento non ha un nome. Ad esempio, l'elemento non dispone di accName implementato e viene restituita una stringa vuota quando viene usato il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) per recuperare il nome MSAA dell'elemento.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate e a una tastiera per la navigazione, perché un elemento potrebbe essere identificato erroneamente dall'utente.

## <a name="possible-causes"></a>Possibili cause

-   L'elemento o il relativo elemento padre non dispone di un nome o di un'etichetta.
-   All'elemento viene assegnato un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) che suggerisce che l'elemento ha un nome.
-   L'elemento con lo stato attivo non deve ricevere lo stato attivo. Ad esempio, un'etichetta o un controllo disabilitato.
-   Un controllo invisibile ha ricevuto lo stato attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




