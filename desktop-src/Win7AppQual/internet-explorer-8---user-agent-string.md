---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882614"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-stringa agente utente

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows XP Windows \| Vista Windows \| 7  
**Server** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -alta  











## <a name="description"></a>Descrizione

La stringa agente utente è l'identificatore di Internet Explorer che fornisce i dati sulla versione e altri attributi ai server Web. Molte applicazioni Web si basano su e su Piggyback, la stringa dell'agente utente di IE. Verranno ripercussioni le operazioni che consentono di eseguire questa operazione e che dipendono da un numero di versione precedente. La stringa agente utente include ora la stringa "Trident/4.0" per consentire la differenziazione tra la stringa agente utente Internet Explorer 7 e la stringa agente utente di Internet Explorer 8 durante l'esecuzione in visualizzazione compatibilità di Internet Explorer 7. Per informazioni dettagliate, vedere informazioni sulle stringhe agente utente.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Sono presenti due aree interessate:

-   Le pagine Web che controllano in modo esplicito la stringa agente utente e non supportano la stringa agente utente Internet Explorer 8 potrebbero non funzionare correttamente. Nella maggior parte dei casi, ciò significa che le pagine bloccano gli utenti dal contenuto a cui tentano di accedere o visualizzano contenuto non corretto o non valido.
-   Le applicazioni che ospitano Trident (vedere Hosting e riuso) utilizzeranno per impostazione predefinita Internet Explorer 7 utilizzando il componente facoltativo Web, ma non avranno accesso alle funzionalità di Internet Explorer 8.

## <a name="solution"></a>Soluzione

Verificare che le applicazioni gestiscano correttamente la nuova versione di ' MSIE 8,0' nella stringa agente utente. È inoltre possibile acconsentire esplicitamente alla visualizzazione di compatibilità di Internet Explorer 7 per le applicazioni basate su Internet Explorer 7. Questa operazione può essere eseguita con i tag meta. Per informazioni dettagliate, vedere la discussione in informazioni sulle stringhe agente utente.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

-   Eseguire le applicazioni e le pagine Web in un ambiente Internet Explorer 8 in Windows Vista o Windows XP per assicurarsi che si comportino nel modo desiderato.
-   In alternativa, è possibile eseguire lo strumento di test della compatibilità di Internet Explorer (IECTT) fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi causati da aggiornamenti delle funzionalità di sicurezza.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Informazioni sulle stringhe agente utente](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Stringa di User-Agent di Internet Explorer 8](/archive/blogs/ie/)
-   [Stringa dell'agente utente e vettore della versione](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hosting e riutilizzo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Download di Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Problemi noti relativi alle funzionalità di sicurezza di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
