---
title: Creazione dinamica del documento ServiceInfo
description: Creazione dinamica del documento ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player online, creazione di un documento ServiceInfo
- negozi online, creazione di un documento ServiceInfo
- tipo 1 negozi online, creazione di documento ServiceInfo
- store online di tipo 2, creazione di un documento ServiceInfo
- Windows Media Player online, creazione dinamica di documento ServiceInfo
- negozi online, creazione dinamica di un documento ServiceInfo
- tipo 1 negozi online, creazione dinamica di documento ServiceInfo
- store online di tipo 2, creazione dinamica di un documento ServiceInfo
- Windows Media Player online, documento ServiceInfo
- negozi online, documento ServiceInfo
- tipo 1 negozi online, documento ServiceInfo
- store online di tipo 2, documento ServiceInfo
- creazione dinamica di un documento ServiceInfo
- creazione di un documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340991"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Creazione dinamica del documento ServiceInfo

È possibile usare ASP per creare il documento ServiceInfo. In questo modo è possibile ottenere maggiore flessibilità nello store online usando le tecniche seguenti:

-   Generazione dinamica del nome host per gli URL.
-   Modifica degli URL per la localizzazione in base alle impostazioni locali e ai parametri geoid.
-   Aggiunta dinamica dei parametri della stringa di query dall'URL ServiceInfo ad altri URL, ad esempio l'URL della pagina di navigazione.

Il codice di esempio seguente illustra una semplice pagina ASP che crea dinamicamente un documento ServiceInfo:


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



Il codice di esempio precedente usa ASP per recuperare il nome host dal server Web e creare dinamicamente gli URL nel documento. Il codice recupera anche il parametro della *stringa* di query delle impostazioni locali dalla richiesta ServiceInfo e lo aggiunge all'URL per la pagina di navigazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navigazione per i negozi online di tipo 2**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo per uno Store online di tipo 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo per uno store online di tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




