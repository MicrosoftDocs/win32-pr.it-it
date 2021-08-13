---
title: Finestra del client MDI (riferimento all'elemento DELL'interfaccia utente MSAA)
description: L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows. Un'applicazione MDI consente a un utente di usare più di un documento alla volta.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff8279e9934c953e30a7d91710565562cb538d3140d971b1f74ff8963ca7345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565132"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Finestra del client MDI (riferimento all'elemento DELL'interfaccia utente MSAA)

L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows. Un'applicazione MDI consente a un utente di usare più di un documento alla volta.

Un'applicazione MDI ha tre tipi di finestre: una finestra cornice, una finestra client e una serie di finestre figlio. La finestra cornice è simile alla finestra principale di un'applicazione e racchiude la finestra client. La finestra client è un elemento figlio della finestra cornice e funge da sfondo per le finestre figlio. La finestra client fornisce anche il supporto per la creazione e la modifica delle finestre figlio in cui vengono visualizzati i documenti.

Il nome della classe della finestra per una finestra client MDI è "MDIClient".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una finestra client MDI supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una finestra client MDI supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **proprietà ChildCount** è il numero di finestre figlio in cui vengono visualizzati i documenti.                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **proprietà Name** è "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **proprietà Parent** è la finestra cornice MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **proprietà Role** è ROLE SYSTEM [**\_ \_ CLIENT**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **proprietà State** è una combinazione di uno o più dei valori [seguenti:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





