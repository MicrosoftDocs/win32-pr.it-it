---
title: Finestra client MDI (riferimento all'elemento MSAA UI)
description: L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows. Un'applicazione MDI consente a un utente di usare più di un documento alla volta.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955426"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Finestra client MDI (riferimento all'elemento MSAA UI)

L'interfaccia a documenti multipli (MDI) è una specifica che definisce l'interfaccia utente standard per le applicazioni scritte per Windows. Un'applicazione MDI consente a un utente di usare più di un documento alla volta.

Un'applicazione MDI dispone di tre tipi di finestre: una finestra cornice, una finestra client e un numero di finestre figlio. La finestra cornice è simile alla finestra principale di un'applicazione e racchiude la finestra del client. La finestra del client è un elemento figlio della finestra cornice e funge da sfondo per le finestre figlio. La finestra client fornisce inoltre supporto per la creazione e la modifica delle finestre figlio in cui vengono visualizzati i documenti.

Il nome della classe di finestra per una finestra client MDI è "MDIClient".

## <a name="iaccessible-methods"></a>Metodi IAccessible

Una finestra client MDI supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Una finestra client MDI supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                 | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La proprietà **childCount** è il numero di finestre figlio in cui vengono visualizzati i documenti.                                                                                                                                                                                                                                                                                                                                                                              |
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La proprietà **Name** è "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La proprietà **Parent** è la finestra cornice MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La proprietà **Role** è [**un \_ \_ client di sistema del ruolo**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ottenere \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La proprietà **state** è costituita da una combinazione di uno o più dei [valori](object-state-constants.md)seguenti: stato sistema [**\_ \_ invisibile**](object-state-constants.md) allo stato sistema stato \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ inattivo**](object-state-constants.md) sistema stato non disponibile<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





