---
title: Funzionamento di WM_GETOBJECT
description: Microsoft Active Accessibility invia il \_ messaggio WM GetObject all'applicazione server appropriata quando un client chiama una delle funzioni AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe287bca68c925cb7be95ff52d2dac547ed097
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337671"
---
# <a name="how-wm_getobject-works"></a>Funzionamento di WM \_ GETobject

Microsoft Active Accessibility invia il messaggio [**WM \_ GetObject**](wm-getobject.md) all'applicazione server appropriata quando un client chiama una delle funzioni **AccessibleObjectFrom * * * X* . Nell'elenco seguente vengono descritti i vari scenari che si verificano:

-   Se la finestra o il controllo che [**riceve \_ WM GetObject**](wm-getobject.md) implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la finestra restituisce un riferimento all'interfaccia **IAccessible** usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, insieme alla libreria di Component Object Model (COM), esegue il marshalling appropriato e passa di nuovo il puntatore di interfaccia dal server al client.
-   Se la finestra che riceve il messaggio non implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), deve restituire zero.
-   Se la finestra non gestisce il messaggio [**WM \_ GetObject**](wm-getobject.md) , la funzione [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) restituisce zero.

Anche se il server restituisce zero, Microsoft Active Accessibility fornisce al client le informazioni relative all'oggetto. Per la maggior parte degli oggetti forniti dal sistema, ad esempio caselle di riepilogo e pulsanti, Microsoft Active Accessibility fornisce informazioni complete. per gli altri oggetti, le informazioni sono limitate. Microsoft Active Accessibility, ad esempio, non fornisce informazioni per i controlli che non dispongono di un handle di finestra. Microsoft Active Accessibility restituisce un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con proxy che il client utilizza per ottenere informazioni sull'oggetto.

Per ulteriori informazioni, vedere [il \_ messaggio WM GetObject](the-wm-getobject-message.md).

 

 