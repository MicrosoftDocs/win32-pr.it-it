---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modalità protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882610"
---
# <a name="protected-mode"></a>Modalità protetta

La maggior parte delle funzionalità di sicurezza di Windows Internet Explorer 8 sono disponibili in Internet Explorer 8 per il sistema operativo Windows XP con Service Pack 2 (SP2) e versioni successive. La modalità protetta è disponibile solo per Windows Vista o versioni successive perché si basa sulle seguenti funzionalità di sicurezza nuove per Windows Vista:

-   Il [controllo dell'account utente](https://msdn.microsoft.com/library/aa511445.aspx) facilita l'esecuzione senza privilegi di amministratore. Quando gli utenti eseguono programmi con privilegi utente limitati, è più sicuro da un attacco rispetto a quando vengono eseguiti con privilegi di amministratore. Il sistema operativo Windows può limitare l'esecuzione di azioni dannose da parte del codice dannoso.
-   Un meccanismo di integrità limita l'accesso in scrittura agli [oggetti a protezione diretta](../secauthz/securable-objects.md) mediante processi di integrità inferiore, nello stesso modo in cui l'appartenenza a un gruppo di account utente limita i diritti di accesso degli utenti ai componenti di sistema sensibili.
-   L' [isolamento dei privilegi dell'interfaccia utente (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impedisce ai processi di inviare messaggi della finestra selezionati e altre API utente ai processi in esecuzione con maggiore integrità.

L'infrastruttura di sicurezza di Windows Integrity Mechanism consente la modalità protetta per fornire a Windows Internet Explorer i privilegi necessari agli utenti per esplorare il Web, negando al tempo stesso i privilegi necessari agli utenti per l'installazione automatica dei programmi o la modifica dei dati di sistema sensibili.

Gli utenti possono disabilitare questa funzionalità tramite una casella di controllo e gli amministratori possono disabilitarla utilizzando Criteri di gruppo.

> [!IMPORTANT]
> È necessario disabilitare la funzionalità solo come misura temporanea durante la risoluzione dei problemi per confrontare il comportamento dell'applicazione quando la funzionalità è abilitata o meno. Si consiglia di lasciare la funzionalità abilitata in modo permanente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
