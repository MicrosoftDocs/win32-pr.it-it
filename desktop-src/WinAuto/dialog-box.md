---
title: Finestra di dialogo (riferimento all'elemento dell'interfaccia utente MSAA)
description: Una finestra di dialogo è una finestra temporanea creata da un'applicazione per recuperare l'input dell'utente.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727535"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Finestra di dialogo (riferimento all'elemento dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti della finestra di **dialogo** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La procedura per la creazione di oggetti **finestra di dialogo** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Una finestra di dialogo è una finestra temporanea creata da un'applicazione per recuperare l'input dell'utente. In un'applicazione vengono utilizzate finestre di dialogo per richiedere all'utente ulteriori informazioni sui comandi scelti dall'utente da un menu. Una finestra di dialogo contiene uno o più controlli (finestre figlio) con cui l'utente immette il testo, sceglie le opzioni o indirizza l'azione del comando.

Il nome della classe della finestra per le finestre di dialogo è " \# 32770".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una finestra di dialogo supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Metodo                                                                    | Commenti                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Se la finestra di dialogo contiene un pulsante di push predefinito, il metodo [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) chiama [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con il messaggio del pulsante di [**\_ clic della BM**](/windows/desktop/Controls/bm-click) per fare clic sul pulsante di push predefinito. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una finestra di dialogo supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | La proprietà **childCount** è uguale al numero di controlli finestra figlio nella finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Se la finestra di dialogo contiene un pulsante di push predefinito, la proprietà **DefaultAction** è "premere".                                                                                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | In genere, le finestre di dialogo non dispongono di tasti di scelta rapida. Se il testo della finestra per la finestra di dialogo contiene un carattere e commerciale (&), Microsoft Active Accessibility restituisce una stringa non null come proprietà **KeyboardShortcut** .                                                                                                                                                                                                                                        |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | La proprietà **Name** è il testo della finestra, o didascalia, che viene visualizzata nella barra del titolo della finestra di dialogo.                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | La proprietà **Parent** è una finestra ( [**\_ \_ finestra del sistema di ruoli**](object-roles.md) ) che racchiude la finestra di dialogo e ha la stessa proprietà **Name** e il nome della classe Window della finestra di dialogo.                                                                                                                                                                                                                                                        |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | La proprietà **Role** è la [**finestra di \_ \_ dialogo del sistema dei ruoli**](object-roles.md) o il sistema del [**ruolo \_ \_ PROPERTYPAGE**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto finestra di dialogo non supporta il metodo [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) . Per ottenere un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo in una finestra di dialogo, i client devono ottenere l'handle della finestra del controllo, quindi chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

