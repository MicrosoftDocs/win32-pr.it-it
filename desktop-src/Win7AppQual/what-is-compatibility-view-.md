---
description: .
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: Che cos'è la visualizzazione compatibilità?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac72fc5afa0e2946a4f904cbcea3c7b0af723c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760784"
---
# <a name="what-is-compatibility-view"></a>Che cos'è la visualizzazione compatibilità?

*Visualizzazione compatibilità* è una funzionalità di Windows Internet Explorer 8 che consente al browser di eseguire il rendering di una pagina Web in modo quasi identico al modo in cui viene eseguito il rendering di Windows Internet Explorer 7.

In Internet Explorer 8 la visualizzazione compatibilità modifica il modo in cui il browser interpreta il codice scritto in CSS, HTML e il Document Object Model (DOM) per tentare di trovare la corrispondenza con Internet Explorer 7. Un sito che un utente Visualizza nella visualizzazione di compatibilità di Internet Explorer 8 è quasi identico a un sito che l'utente visualizza in Internet Explorer 7. Tuttavia, la visualizzazione compatibilità non modifica il modo in cui il browser interpreta tutto il codice. Ad esempio, le modifiche apportate a Internet Explorer 8 per il modo in cui il browser gestisce ActiveX, il parser, AJAX, JavaScript, rete e sicurezza potrebbero comunque causare problemi di compatibilità. La visualizzazione compatibilità non modifica questi comportamenti.

In un ambito aziendale, alcune aree presentano un rischio ridotto per quanto riguarda i problemi di compatibilità. Ad esempio, i siti Web dell'area Intranet utilizzano Visualizzazione Compatibilità per impostazione predefinita. Anche le applicazioni Web client che eseguono il rendering tramite il controllo Web browser o WebOC (motore di rendering di Internet Explorer) presentano un basso rischio di problemi di compatibilità poiché Internet Explorer 8 USA per impostazione predefinita una modalità di compatibilità per il WebOC. Tuttavia, le impostazioni di configurazione predefinite per la visualizzazione compatibilità potrebbero non garantire la compatibilità completa. Per determinare se un sito Web o un'applicazione Web è compatibile con Internet Explorer 8, è necessario testare il sito Web o l'applicazione Web.

Per ulteriori informazioni sulle differenze tra la visualizzazione compatibilità di Internet Explorer 8 e Internet Explorer 7, vedere il Blog relativo alla [compatibilità del sito e a Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8). Per un elenco degli elementi da controllare quando si esegue l'aggiornamento a Internet Explorer 8, vedere il [Toolkit di conformità di Internet Explorer 8](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).

Per ulteriori informazioni sulla visualizzazione compatibilità, vedere il [Blog del team di Internet Explorer](/archive/blogs/ie/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
