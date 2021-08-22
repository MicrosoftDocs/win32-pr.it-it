---
title: Informazioni sui problemi di prestazioni
description: Questo argomento descrive i problemi di prestazioni associati all'uso dei pattern di controllo Text e TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- client, informazioni sui problemi di prestazioni
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo del testo
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861221"
---
# <a name="understanding-performance-issues"></a>Informazioni sui problemi di prestazioni

Questo argomento descrive i problemi di prestazioni associati all'uso dei pattern di controllo Text e [TextRange.](uiauto-implementingtextandtextrange.md)


Le [**interfacce IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) si basano su chiamate tra processi. Non forniscono un meccanismo di memorizzazione nella cache per migliorare le prestazioni durante il recupero o l'elaborazione di contenuto testuale.

Un'applicazione client può migliorare le prestazioni usando il [**metodo IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) per recuperare blocchi di testo di dimensioni moderate. Ad esempio, l'uso di **GetText** per recuperare singoli caratteri comporta un miglioramento delle prestazioni tra processi per ogni carattere, mentre non specificando una lunghezza massima quando si chiama **GetText** si verifica un solo hit cross-process, ma può avere una latenza elevata a seconda delle dimensioni dell'intervallo di testo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automazione interfaccia utente supporto per il contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




