---
title: Oggetto client (riferimento all'elemento DELL'interfaccia utente MSAA)
description: L'area client è la parte di una finestra in cui l'applicazione visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop visualizza la pagina corrente di un documento nell'area client.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645061"
---
# <a name="client-object-msaa-ui-element-reference"></a>Oggetto client (riferimento all'elemento DELL'interfaccia utente MSAA)

L'area client è la parte di una finestra in cui l'applicazione visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop visualizza la pagina corrente di un documento nell'area client.

Gli sviluppatori di applicazioni server sono responsabili della creazione di oggetti accessibili che forniscono informazioni sul contenuto dell'area client dell'applicazione.

Se un'applicazione client richiede informazioni su un elemento dell'interfaccia utente personalizzato all'interno di un'applicazione e l'elemento dell'interfaccia utente personalizzato che non supporta [**l'interfaccia IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Microsoft Active Accessibility crea un oggetto accessibile predefinito con informazioni minime.

## <a name="iaccessible-methods"></a>Metodi IAccessible

L'area client supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

L'area client supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                             | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Invia il [**messaggio WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) per recuperare il testo della finestra.                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La **proprietà Role** è ROLE SYSTEM [**\_ \_ CLIENT**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md)[**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

