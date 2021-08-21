---
title: Testo statico (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: I controlli testo statico offrono un modo pratico per visualizzare testo nelle finestre di dialogo e in altre finestre. I controlli di testo statico spesso fungono da etichette per altri controlli.
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052489"
---
# <a name="static-text-msaa-ui-element-reference"></a>Testo statico (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

I controlli testo statico offrono un modo pratico per visualizzare testo nelle finestre di dialogo e in altre finestre. I controlli di testo statico spesso fungono da etichette per altri controlli.

Il nome della classe della finestra per un controllo di testo statico è "STATIC".

## <a name="iaccessible-methods"></a>Metodi IAccessible

I controlli testo statico supportano i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

I controlli testo statico supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La **proprietà ChildCount** è zero.                                                                                                                                                                                                                                                          |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta, ovvero il carattere sottolineato nel testo che attiva il controllo associato al testo statico. La stringa restituita contiene il carattere del tasto di scelta aggiunto alla stringa "ALT+".                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** corrisponde al testo nel controllo testo statico.                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà Parent è una finestra ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md)  ) che racchiude il controllo e ha la stessa proprietà **Name** e lo stesso nome della classe della finestra del controllo.                                                                                   |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ STATICTEXT.**](object-roles.md)                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)STATE SYSTEM [**\_ \_ READONLY**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

-   Il [**metodo accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) restituisce DISP E MEMBERNOTFOUND quando viene \_ chiamato con \_ [**SELFLAG \_ TAKEFOCUS**](selflag.md) su un oggetto testo statico.
-   I controlli statici con stile SS \_ ICON restituiscono dati non validi nella **proprietà** Name.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





