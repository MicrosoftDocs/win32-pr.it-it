---
title: Creazione dinamica del documento ServiceInfo
description: Creazione dinamica del documento ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player Online Stores, creazione di un documento ServiceInfo
- archivi online, creazione di un documento ServiceInfo
- digitare 1 negozi online, creazione del documento ServiceInfo
- digitare 2 archivi online, creazione del documento ServiceInfo
- Windows Media Player Online Stores, creazione dinamica del documento ServiceInfo
- negozi online, creazione dinamica di documenti ServiceInfo
- digitare 1 negozi online, creazione dinamica del documento ServiceInfo
- digitare 2 archivi online, creazione dinamica del documento ServiceInfo
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- creazione dinamica di un documento ServiceInfo
- creazione del documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955181"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Creazione dinamica del documento ServiceInfo

Per creare il documento ServiceInfo, è possibile utilizzare ASP. Questo consente di ottenere una maggiore flessibilità nel negozio online usando le tecniche seguenti:

-   Generazione dinamica del nome host per gli URL.
-   Modifica degli URL per la localizzazione in base ai parametri delle impostazioni locali e di Geoid.
-   Accodare dinamicamente i parametri della stringa di query dall'URL ServiceInfo ad altri URL, ad esempio l'URL della pagina Navigate.

Il codice di esempio seguente mostra una pagina ASP semplice che crea dinamicamente un documento ServiceInfo:


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



Il codice di esempio precedente utilizza ASP per recuperare il nome host dal server Web e creare in modo dinamico gli URL nel documento. Il codice recupera anche il parametro della stringa di query delle *impostazioni locali* dalla richiesta ServiceInfo e lo aggiunge all'URL per la pagina Navigate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navigazione per i negozi di tipo 2 online**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo per un negozio online di tipo 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo per un negozio online di tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




