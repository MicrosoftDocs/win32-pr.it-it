---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829530"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Testo

L'elemento non ha un nome

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento non ha un nome. Ad esempio, l'elemento non ha accName implementato e viene restituita una stringa vuota quando viene usato il metodo [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) per recuperare il nome MSAA dell'elemento.

Questo problema causa problemi per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per lo spostamento perché un elemento potrebbe essere identificato in modo non corretto per l'utente.

## <a name="possible-causes"></a>Possibili cause

-   L'elemento o il relativo elemento padre non ha nome o etichetta.
-   All'elemento viene assegnato [**un accRole che**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) suggerisce che l'elemento ha un nome.
-   L'elemento con lo stato attivo non deve ricevere lo stato attivo. Ad esempio, un'etichetta o un controllo disabilitato.
-   Un controllo invisibile ha ricevuto lo stato attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> </dl>

 

 




