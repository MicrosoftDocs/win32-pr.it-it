---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940e1242be2b0393023bc83b31cc662a52677c59307dff01fed30d8319604d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827397"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Testo

L'elemento è un elemento AutomationElement orfano nell'albero

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'indirizzo dell'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dell'oggetto ottenuto per le coordinate specificate è un riferimento a un elemento orfano nell'albero degli elementi.

Questo problema è un problema per gli utenti che si affidano a un'utilità per la lettura dello schermo e a una tastiera per la navigazione, perché gli elementi verranno considerati invisibili e non verranno annunciati all'utente.

## <a name="possible-causes"></a>Possibili cause

-   L'interazione dell'utente durante la verifica, ad esempio lo spostamento dello stato attivo su un HWND non di destinazione, ha interferito con il processo di verifica.
-   Implementazione di un Automazione interfaccia utente non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




