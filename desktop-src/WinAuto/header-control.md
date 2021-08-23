---
title: Controllo Header (riferimento all'elemento DELL'interfaccia utente MSAA)
description: Un controllo intestazione visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni. Windows Explorer usa un controllo intestazione quando è selezionata la visualizzazione Dettagli.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c378bb0244e94f4cb95c8b2ba90512d2b17542bdef7428197ee58479dbfde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994181"
---
# <a name="header-control-msaa-ui-element-reference"></a>Controllo Header (riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Controllo intestazione** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Controllo intestazione** in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Un controllo intestazione visualizza le intestazioni nella parte superiore delle colonne di informazioni e consente all'utente di ordinare le informazioni facendo clic sulle intestazioni. Windows Explorer usa un controllo intestazione quando è selezionata la visualizzazione Dettagli.

Il nome della classe della finestra per un controllo intestazione è WC HEADER, definito \_ come "SysHeader32" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo intestazione supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Questo metodo esegue l'azione predefinita facendo clic sull'intestazione. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo intestazione supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                       | Commenti                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La **proprietà ChildCount** è zero.                                                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | La **proprietà DefaultAction** è "Click".                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | La **proprietà Name** corrisponde al nome dell'intestazione di colonna.                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | La **proprietà Parent** è una finestra ( ROLE SYSTEM [**\_ \_ LIST**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo.                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | La **proprietà Role** è ROLE SYSTEM [**\_ \_ COLUMNHEADER.**](object-roles.md)                                                                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | Il valore della proprietà **State** è sempre [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) e può anche includere [**STATE SYSTEM \_ \_ INVISIBLE.**](object-state-constants.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




