---
description: Modalità protetta
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modalità protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116449"
---
# <a name="protected-mode"></a>Modalità protetta

La maggior parte delle funzionalità di sicurezza di Windows Internet Explorer 8 è disponibile in Internet Explorer 8 per il sistema operativo Windows XP con Service Pack 2 (SP2) e versioni successive. La modalità protetta è disponibile solo per Windows Vista o versioni successive perché si basa sulle funzionalità di sicurezza seguenti che non sono nuove di Windows Vista:

-   [Controllo dell'account](https://msdn.microsoft.com/library/aa511445.aspx) utente semplifica l'esecuzione senza privilegi di amministratore. Quando gli utenti eseguono programmi con privilegi utente limitati, sono più sicuri da un attacco rispetto a quando vengono eseguiti con privilegi di amministratore. Il sistema operativo Windows può impedire al codice dannoso di eseguire azioni dannose.
-   Un meccanismo di integrità [](../secauthz/securable-objects.md) limita l'accesso in scrittura agli oggetti a protezione diretta tramite processi con integrità inferiore, nello stesso modo in cui l'appartenenza al gruppo di account utente limita i diritti degli utenti per l'accesso a componenti di sistema sensibili.
-   Interfaccia utente l'isolamento dei privilegi [(UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impedisce ai processi di inviare messaggi finestra selezionati e altre API UTENTE a processi in esecuzione con integrità superiore.

L'infrastruttura di sicurezza del meccanismo di integrità di Windows consente alla modalità protetta di fornire a Windows Internet Explorer i privilegi necessari agli utenti per esplorare il Web, mantenendo al tempo stesso i privilegi necessari agli utenti per installare i programmi in modo invisibile all'utente o modificare i dati sensibili del sistema.

Gli utenti possono disabilitare questa funzionalità tramite una casella di controllo e gli amministratori possono disabilitarla usando Criteri di gruppo.

> [!IMPORTANT]
> È consigliabile disabilitare la funzionalità solo come misura temporanea durante la risoluzione dei problemi per confrontare il comportamento dell'applicazione quando la funzionalità è abilitata o meno. È consigliabile mantenere questa funzionalità abilitata in modo permanente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
