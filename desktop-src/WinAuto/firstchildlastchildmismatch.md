---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3f168357cd67a7f22e81e985042a4983e7d8291bb6a0e2e343753959bcd6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828953"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Testo

Quando ci si sposta chiamando dal nodo testato e quindi chiamando ripetutamente , è stato terminato {0} {1} l'elemento figlio seguente: {2} . Non corrisponde al risultato della chiamata {3} al metodo sul nodo testato, che ha restituito: {4} . L'elemento figlio deve invece segnalare come padre il nodo di test.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Si è verificato un problema durante lo spostamento tra gli elementi figlio dell'elemento. 1. Implementazione non corretta o Automazione interfaccia utente non valida.

Questo problema può causare problemi di navigazione per gli strumenti automatizzati perché l'attraversamento di elementi potrebbe essere imprevedibile e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione non corretta o Automazione interfaccia utente non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




