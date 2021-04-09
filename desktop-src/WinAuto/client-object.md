---
title: Oggetto client (riferimento all'elemento MSAA UI)
description: L'area client è la parte di una finestra in cui l'applicazione Visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop Visualizza la pagina corrente di un documento nell'area client.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117991"
---
# <a name="client-object-msaa-ui-element-reference"></a>Oggetto client (riferimento all'elemento MSAA UI)

L'area client è la parte di una finestra in cui l'applicazione Visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop Visualizza la pagina corrente di un documento nell'area client.

Gli sviluppatori di applicazioni server sono responsabili della creazione di oggetti accessibili che forniscono informazioni sul contenuto dell'area client dell'applicazione.

Se un'applicazione client richiede informazioni su un elemento dell'interfaccia utente personalizzato all'interno di un'applicazione e l'elemento dell'interfaccia utente personalizzato che non supporta l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Microsoft Active Accessibility crea un oggetto accessibile predefinito con informazioni minime.

## <a name="iaccessible-methods"></a>Metodi IAccessible

L'area client supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

L'area client supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Invia il messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) per recuperare il testo della finestra.                                                                                                                                                                                                                                                                                                                                                                                |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La proprietà **Role** è [**un \_ \_ client del sistema Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

