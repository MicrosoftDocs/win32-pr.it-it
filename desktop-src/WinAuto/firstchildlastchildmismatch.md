---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396354"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Testo

Quando si esegue la chiamata {0} dal nodo testato e quindi si chiama ripetutamente {1} , è terminata l'operazione figlio seguente: {2} . Non corrisponde al risultato della chiamata al {3} nodo testato, che ha restituito: {4} . Al contrario, l'elemento figlio deve segnalare come padre il nodo di test.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Si è verificato un problema durante la navigazione tra gli elementi figlio dell'elemento. 1. Implementazione di automazione interfaccia utente non corretta o non valida.

Questo problema può causare problemi di navigazione per gli strumenti automatici perché l'attraversamento degli elementi potrebbe essere irregolare e imprevedibile.

## <a name="possible-causes"></a>Possibili cause

Implementazione di automazione interfaccia utente non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




