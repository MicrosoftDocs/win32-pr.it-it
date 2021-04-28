---
description: Internet Explorer 8 - Stringa agente utente
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8 - Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088239"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8 - Stringa agente utente

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Alta  











## <a name="description"></a>Descrizione

User Agent String è l'identificatore Internet Explorer che fornisce i dati sulla relativa versione e altri attributi ai server Web. Molte applicazioni Web si basano sulla stringa agente utente IE e su cui si basa piggyback. Saranno influenzati quelli che e dipendono da un numero di versione precedente. La stringa Agente utente include ora la stringa "Trident/4.0" per consentire la differenziazione tra la stringa agente utente di Internet Explorer 7 e la stringa agente utente di Internet Explorer 8 durante l'esecuzione in Internet Explorer 7 Visualizzazione Compatibilità. Per informazioni dettagliate, vedere Informazioni sulle stringhe agente utente.

## <a name="manifestation-of-impact"></a>Impatto significativo

Esistono due aree interessate:

-   Le pagine Web che controllano in modo esplicito la stringa agente utente e non supportano la Internet Explorer 8 User Agent String potrebbero non essere eseguite correttamente. Nella maggior parte dei casi, ciò significa che le pagine verranno bloccate dagli utenti dal contenuto a cui tentano di accedere o visualizzare contenuto errato o in formato non corretto.
-   Le applicazioni che ospitano Trident (vedere Hosting e riutilizzo) usano per impostazione predefinita Internet Explorer 7 usando il componente facoltativo Web, ma non avranno accesso Internet Explorer 8 funzionalità.

## <a name="solution"></a>Soluzione

Assicurarsi che le applicazioni gestino correttamente la nuova versione "MSIE 8.0" nella stringa agente utente. È anche possibile acconsentire esplicitamente all'Internet Explorer 7 Visualizzazione Compatibilità per le applicazioni basate su Internet Explorer 7. Questa operazione può essere eseguita con i metatag. Per informazioni dettagliate, vedere la discussione informazioni sulle stringhe agente utente.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

-   Eseguire le applicazioni e le pagine Web in un ambiente Internet Explorer 8 in Windows Vista o Windows XP per assicurarsi che si comportino nel modo desiderato.
-   In alternativa, è possibile eseguire lo strumento Internet Explorer Compatibility Test Tool (IECTT) fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi potenziali dovuti agli aggiornamenti delle funzionalità di sicurezza.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Informazioni sulle stringhe dell'agente utente](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Internet Explorer 8 User-Agent stringa](/archive/blogs/ie/)
-   [Stringa dell'agente utente e vettore di versione](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hosting e riutilizzo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Application Compatibility Toolkit Download](/windows-hardware/get-started/adk-install)
-   [Problemi noti Internet Explorer funzionalità di sicurezza](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
