---
title: Funzionamento di WM_GETOBJECT
description: Microsoft Active Accessibility il messaggio WM GETOBJECT all'applicazione server appropriata quando un client chiama una delle \_ funzioni AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795761"
---
# <a name="how-wm_getobject-works"></a>Funzionamento di WM \_ GETOBJECT

Microsoft Active Accessibility il messaggio [**WM \_ GETOBJECT**](wm-getobject.md) all'applicazione server appropriata quando un client chiama una delle **funzioni AccessibleObjectFrom**_X._ L'elenco seguente descrive i vari scenari che si verificano:

-   Se la finestra o il controllo che riceve [**WM \_ GETOBJECT**](wm-getobject.md) implementa [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)la finestra restituisce un riferimento all'interfaccia **IAccessible** usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, in combinazione con la libreria Component Object Model (COM), esegue il marshalling appropriato e passa il puntatore a interfaccia dal server al client.
-   Se la finestra che riceve il messaggio non implementa [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)deve restituire zero.
-   Se la finestra non gestisce il [**messaggio WM \_ GETOBJECT,**](wm-getobject.md) la [funzione DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) restituisce zero.

Anche se il server restituisce zero, Microsoft Active Accessibility fornisce comunque al client informazioni sull'oggetto . Per la maggior parte degli oggetti forniti dal sistema, ad esempio caselle di riepilogo e pulsanti, Microsoft Active Accessibility informazioni complete. per altri oggetti, le informazioni sono limitate. Ad esempio, Microsoft Active Accessibility non fornisce informazioni per i controlli che non dispongono di un handle di finestra. Microsoft Active Accessibility restituisce un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proxy che il client usa per ottenere informazioni sull'oggetto.

Per altre informazioni, vedere [Messaggio WM \_ GETOBJECT](the-wm-getobject-message.md).

 

 