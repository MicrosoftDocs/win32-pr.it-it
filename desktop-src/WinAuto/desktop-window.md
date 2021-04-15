---
title: Finestra desktop (riferimento all'elemento dell'interfaccia utente MSAA)
description: Nella finestra del desktop viene visualizzata la visualizzazione elenco dei desktop (che contiene icone come Computer locale) e la barra delle applicazioni che contiene il pulsante Avvia.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395491"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Finestra desktop (riferimento all'elemento dell'interfaccia utente MSAA)

Nella finestra del desktop viene visualizzata la visualizzazione elenco dei desktop (che contiene icone come Computer locale) e la barra delle applicazioni che contiene il pulsante **Avvia** .

Questo oggetto viene raramente sottoposto a query dai client perché la visualizzazione elenco e la barra delle applicazioni coprono l'intero desktop. L'oggetto desktop viene recuperato al momento dell'accesso, prima che la shell del sistema operativo visualizzi la visualizzazione elenco e la barra delle applicazioni. In alcuni casi, il desktop viene ottenuto quando ci si sposta da altri oggetti.

Il nome della classe di finestra per la finestra del desktop è " \# 32769".

## <a name="iaccessible-methods"></a>Metodi IAccessible

La finestra desktop supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

La finestra desktop supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La proprietà Name è "desktop".                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** è [**un \_ \_ client del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**ottenere \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





