---
title: Informazioni sui problemi di prestazioni
description: In questo argomento vengono descritti i problemi di prestazioni associati all'utilizzo dei pattern di controllo Text e TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- client, informazioni sui problemi di prestazioni
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo Text
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339723"
---
# <a name="understanding-performance-issues"></a>Informazioni sui problemi di prestazioni

In questo argomento vengono descritti i problemi di prestazioni associati all'utilizzo dei pattern di controllo [Text e TextRange](uiauto-implementingtextandtextrange.md) .


Le interfacce [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) si basano sulle chiamate tra processi, ma non forniscono un meccanismo di memorizzazione nella cache per migliorare le prestazioni durante il recupero o l'elaborazione di contenuto testuale.

Un'applicazione client può migliorare le prestazioni usando il metodo [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) per recuperare blocchi di testo di dimensioni moderate. Ad esempio, l'utilizzo di **gettext** per recuperare singoli caratteri comporterà un riscontro delle prestazioni tra processi per ogni carattere, mentre se non si specifica una lunghezza massima durante la chiamata di **gettext** , viene raggiunto un hit tra processi, ma può avere una latenza elevata a seconda delle dimensioni dell'intervallo di testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




