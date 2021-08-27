---
title: Punto di accesso (riferimenti a elementi dell'interfaccia utente MSAA)
description: Il punto di inserimento è una riga, un blocco o una bitmap lampeggiante nell'area client di una finestra o in un controllo che accetta l'input da tastiera.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467298"
---
# <a name="caret-msaa-ui-element-reference"></a>Punto di accesso (riferimenti a elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive i punti di accesso ai riferimenti all'elemento dell'interfaccia utente MSAA. L'uso dei caret in diversi framework dell'interfaccia utente non è descritto qui. Vedere la documentazione di riferimento dell'API per il framework dell'interfaccia utente in uso.

 

Il punto di inserimento è una riga, un blocco o una bitmap lampeggiante nell'area client di una finestra o in un controllo che accetta l'input da tastiera. Indica la posizione in cui vengono inseriti testo o grafica. Poiché solo una finestra alla volta ha lo stato attivo, nel sistema è presente un solo punto di interesse.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Il caret supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Il caret supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:




| Proprietà | Commenti | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | La <strong>proprietà ChildCount</strong> è zero. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | La <strong>proprietà Name</strong> è "Edit". | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | La <strong>proprietà Role</strong> è <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | I valori possibili per la <strong>proprietà State</strong> includono:<ul><li>Zero, ovvero il punto di controllo è visibile</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>Note

-   A differenza di altri elementi dell'interfaccia utente, all'oggetto punto di controllo non è associato un handle di finestra. Per ottenere l'accesso all'oggetto punto di accesso, i client devono impostare [*un WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e attendere che l'oggetto punto di accesso generi eventi.
-   L'oggetto cursore nel controllo Rich Edit fornito da Riched20.dll (usato in editor di testo come Microsoft WordPad in Windows 98) non invia alcun [WinEvent quando](winevents-infrastructure.md) la relativa posizione viene modificata durante la selezione del testo. Quando gli utenti premono MAIUSC e i tasti di direzione per selezionare il testo, l'oggetto cursore non attiva [**EVENT \_ OBJECT \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Analogamente, quando la selezione viene impostata a livello di codice tramite messaggi rich edit, l'oggetto cursore non invia eventi per indicare la nuova posizione.

    Tutte le applicazioni che usano Riched20.dll presentano questo problema. Le applicazioni che usano versioni precedenti del controllo Rich Edit inviano correttamente gli eventi in base alla selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




