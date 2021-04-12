---
title: Controllo Header (riferimento all'elemento MSAA UI)
description: Un controllo intestazione Visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni. Quando si seleziona la visualizzazione dettagli, Esplora risorse utilizza un controllo intestazione.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331439"
---
# <a name="header-control-msaa-ui-element-reference"></a>Controllo Header (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti **controllo intestazione** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **controllo intestazione** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un controllo intestazione Visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni. Quando si seleziona la visualizzazione dettagli, Esplora risorse utilizza un controllo intestazione.

Il nome della classe di finestra per un controllo intestazione è WC \_ header, definito come "SysHeader32" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo header supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Questo metodo esegue l'azione predefinita facendo clic sull'intestazione. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo header supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                       | Commenti                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La proprietà **childCount** è zero.                                                                                                                                                                                                   |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | La proprietà **DefaultAction** è "click".                                                                                                                                                                                             |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | La proprietà **Name** corrisponde al nome dell'intestazione di colonna.                                                                                                                                                                    |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | La proprietà **Parent** è una finestra ( [**\_ \_ elenco del sistema di ruoli**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo.                                                      |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | La proprietà **Role** è [**Role \_ System \_ COLUMNHEADER**](object-roles.md).                                                                                                                                  |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Il valore della proprietà **state** è sempre [**state \_ System \_ ReadOnly**](object-state-constants.md) e può includere anche il [**sistema di stato \_ \_ invisibile**](object-state-constants.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




