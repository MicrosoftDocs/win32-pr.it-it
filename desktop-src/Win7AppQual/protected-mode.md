---
description: Modalità protetta
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modalità protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2f16b9f923215af6c2211339859d8eab4803e6793be248a83760e298ed084c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994781"
---
# <a name="protected-mode"></a>Modalità protetta

La maggior Windows Internet Explorer 8 funzionalità di sicurezza sono disponibili in Internet Explorer 8 per il sistema operativo Windows XP con Service Pack 2 (SP2) e versioni successive. La modalità protetta è disponibile solo per Windows Vista o versioni successive perché si basa sulle funzionalità di sicurezza seguenti che non sono Windows Vista:

-   [Controllo dell'account](https://msdn.microsoft.com/library/aa511445.aspx) utente semplifica l'esecuzione senza privilegi di amministratore. Quando gli utenti eseguono programmi con privilegi utente limitati, sono più sicuri da un attacco rispetto a quando vengono eseguiti con privilegi di amministratore. Il Windows sistema operativo può impedire al codice dannoso di eseguire azioni dannose.
-   Un meccanismo di integrità [](../secauthz/securable-objects.md) limita l'accesso in scrittura agli oggetti a protezione diretta tramite processi di integrità inferiore, nello stesso modo in cui l'appartenenza al gruppo di account utente limita i diritti degli utenti per accedere ai componenti di sistema sensibili.
-   [Interfaccia utente Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impedisce ai processi di inviare messaggi di finestra selezionati e altre API UTENTE ai processi in esecuzione con integrità superiore.

L'infrastruttura di sicurezza del meccanismo di integrità Windows consente alla modalità protetta di fornire Windows Internet Explorer i privilegi necessari agli utenti per esplorare il Web, mantenendo al tempo stesso i privilegi necessari per installare i programmi in modalità invisibile all'utente o modificare i dati sensibili del sistema.

Gli utenti possono disabilitare questa funzionalità tramite una casella di controllo e gli amministratori possono disabilitarla usando Criteri di gruppo.

> [!IMPORTANT]
> È consigliabile disabilitare la funzionalità solo come misura temporanea durante la risoluzione dei problemi per confrontare il comportamento dell'applicazione quando la funzionalità è abilitata o meno. È consigliabile mantenere questa funzionalità abilitata in modo permanente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
