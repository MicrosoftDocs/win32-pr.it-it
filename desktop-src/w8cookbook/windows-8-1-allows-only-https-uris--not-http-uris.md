---
title: URI in Windows 8.1
description: Windows 8.1 solo uri https, non URI HTTP
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3246cad0fb6114a3a01d781ed990e0c277547e2b9ee489572c8124a23e7e81b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028809"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 solo uri https, non URI HTTP

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Server - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

Anche se le app create per Windows 8 possono includere URI http e https negli URI del contenuto dell'applicazione, le app create per Windows 8.1 possono includere solo URI https.

L'unica eccezione è per contentUriRules dinamici specificati nel file di AppxManifest.xml'app. Con ContentUriRules dinamico, le app possono accedere ad altri domini o risorse di rete forniti dall'amministratore, ad esempio Criteri di gruppo URI. Tuttavia, contentUriRules dinamico è disponibile solo per le app Windows Store se soddisfano queste condizioni:

-   La Criteri di gruppo è abilitata
-   Il pacchetto ha specificato la funzionalità enterpriseAuthentication
-   OSMaxVersionTested del pacchetto è Windows 8.1 o versione successiva

Le nuove restrizioni in Windows 8.1 sono parte di restrizioni di sicurezza avanzate per proteggere ulteriormente la piattaforma.

## <a name="manifestations"></a>Manifestazioni

Quando si esegue un'app Windows 8 in Windows 8.1, è consentito l'uso di URI HTTP in [ApplicationContentUriRules.](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)

## <a name="mitigations"></a>Soluzioni di prevenzione

È consigliabile che gli sviluppatori WWA passano dal controllo [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-webview>). Tuttavia, se è necessario il supporto per AppCache, IndexedDB, georilevazione o accesso agli Appunti a livello di codice, è necessario continuare a usare <iframe> per Windows 8.1.

Utilizzo continuo di <iframe> per il contenuto remoto sarà necessaria una nuova voce in ApplicationContentUriRules per l'app. Le app con WebView richiedono nuove voci in ApplicationContentUriRules se il contenuto Web deve richiamare window.external.notify per generare un [evento ScriptNotify.](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) Se non si dispone di Visual Studio, è possibile aggiornare il manifesto dell'app aggiungendo il codice XML seguente, inclusi i caratteri jolly per i sottodomini (ad esempio https:// \* .microsoft.com):


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Risorse

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe> oggetto \| <iframe> element](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Classe Webview](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView.ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 