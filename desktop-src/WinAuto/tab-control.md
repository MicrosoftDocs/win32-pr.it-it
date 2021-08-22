---
title: Controllo Tab (riferimento all'elemento DELL'interfaccia utente MSAA)
description: Un controllo Struttura a schede definisce più pagine per la stessa area di una finestra o di una finestra di dialogo.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fe3216194da590b0c0802343afc41b1f7765c13d194e533163f9af2c22b287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505661"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Controllo Tab (riferimento all'elemento DELL'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **Controllo Struttura a schede** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti Controllo struttura a** schede in vari framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

Un controllo Struttura a schede definisce più pagine per la stessa area di una finestra o di una finestra di dialogo. Ogni pagina è costituita da un set di informazioni o da un gruppo di controlli visualizzati da un'applicazione quando l'utente seleziona la scheda corrispondente. Il Windows operativo usa i controlli struttura a schede per visualizzare i pulsanti della barra delle applicazioni, ad eccezione del **pulsante** Start.

Il nome della classe finestra per un controllo Struttura a schede è TABCONTROL WC, definito \_ come "SysTabControl" in Commctrl.h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo Struttura a schede supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Metodo                                                                    | Commenti                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il [**metodo accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sulla scheda della pagina. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo Struttura a schede supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La **proprietà DefaultAction** è "Switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La **proprietà KeyboardShortcut** è il tasto di scelta del controllo struttura a schede, ovvero un carattere sottolineato nel testo della finestra del controllo. Questa stringa contiene il carattere del tasto di scelta aggiunto alla stringa "ALT+".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La **proprietà Name** viene ottenuta dal testo (o didascalia) della finestra del controllo, che viene visualizzato all'interno del controllo struttura a schede.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La **proprietà Parent** è una finestra ( ROLE SYSTEM [**\_ \_ PAGETABLIST**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome di classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ PAGETAB.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SELECTABLE STATE**](object-state-constants.md) SYSTEM SELECTED STATE SYSTEM \| [**\_ \_ SELECTED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ PRESSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Note

I controlli Struttura a schede restituiscono erroneamente S \_ OK dal [**metodo accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) quando vengono chiamati con il flag [**SELFLAG \_ TAKEFOCUS.**](selflag.md) I controlli Struttura a schede non possono assumere lo stato attivo della tastiera.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





