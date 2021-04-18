---
title: Controllo Tab (riferimento all'elemento MSAA UI)
description: Un controllo struttura a schede definisce più pagine per la stessa area di una finestra o di una finestra di dialogo.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cc8381a668701446e06df81694941ece9f5f259
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298024"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Controllo Tab (riferimento all'elemento MSAA UI)

> [!Note]  
> In questo argomento vengono descritti gli oggetti **controllo scheda** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti controllo struttura a **schede** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Un controllo struttura a schede definisce più pagine per la stessa area di una finestra o di una finestra di dialogo. Ogni pagina è costituita da un set di informazioni o da un gruppo di controlli visualizzati da un'applicazione quando l'utente seleziona la scheda corrispondente. Il sistema operativo Windows utilizza i controlli struttura a schede per visualizzare i pulsanti della barra delle applicazioni, ad eccezione del pulsante **Avvia** .

Il nome della classe della finestra per un controllo struttura a schede è WC \_ TABCONTROL, definito come "SysTabControl" in commctrl. h.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Un controllo struttura A schede supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) fa clic sulla scheda della pagina. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Un controllo struttura A schede supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La proprietà **DefaultAction** è "switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La proprietà **KeyboardShortcut** è la chiave di accesso del controllo Tab, che è un carattere sottolineato nel testo della finestra del controllo. Questa stringa contiene il carattere di chiave di accesso aggiunto alla stringa "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La proprietà **Name** viene ottenuta dal testo o dalla didascalia della finestra del controllo, che viene visualizzata nel controllo struttura a schede.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La proprietà **Parent** è una finestra ( [**Role \_ System \_ PAGETABLIST**](object-roles.md) ) che racchiude il controllo e ha lo stesso nome della classe della finestra del controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**\_ \_ PaginaScheda del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: [**stato \_ sistema \_ invisibile**](object-state-constants.md) stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ selezionato**](object-state-constants.md) stato attivo \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema stato stato attivo<br/> |



 

## <a name="notes"></a>Note

I controlli struttura a schede restituiscono erroneamente S \_ OK dal metodo [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) quando viene chiamato con il flag [**SELFLAG \_ TAKEFOCUS**](selflag.md) . I controlli struttura a schede non possono assumere lo stato attivo della tastiera.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





