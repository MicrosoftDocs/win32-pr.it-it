---
title: URI in Windows 8.1
description: Windows 8.1 solo gli URI https, non gli URI HTTP
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022485f9fc5dc2657127f7bae49127e0bd3b5954
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886119"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 solo gli URI https, non gli URI HTTP

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Server - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

Anche se le app create per Windows 8 possono includere URI http e https negli URI del contenuto dell'applicazione, le app create per Windows 8.1 possono includere solo URI https.

L'unica eccezione è per contentUriRules dinamici specificati nel file di AppxManifest.xml'app. Con ContentUriRules dinamico, le app possono accedere a domini aggiuntivi o risorse di rete fornite dall'amministratore, ad esempio Criteri di gruppo URI. Tuttavia, contentUriRules dinamico è disponibile solo per le app Windows Store se soddisfano queste condizioni:

-   La Criteri di gruppo è abilitata
-   Il pacchetto ha specificato la funzionalità enterpriseAuthentication
-   OSMaxVersionTested del pacchetto è Windows 8.1 o versione successiva

Le nuove restrizioni in Windows 8.1 sono parte di restrizioni di sicurezza avanzate per proteggere ulteriormente la piattaforma.

## <a name="manifestations"></a>Manifestazioni

Quando si esegue un'app Windows 8 in Windows 8.1, è consentito l'uso di URI HTTP in [ApplicationContentUriRules.](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)

## <a name="mitigations"></a>Soluzioni di prevenzione

È consigliabile che gli sviluppatori WWA [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) passano dal controllo [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) ( &lt; x-ms-webview &gt; ). Tuttavia, se è necessario il supporto per AppCache, IndexedDB, georilevazione o accesso agli Appunti a livello di codice, è necessario continuare a usare <iframe> per Windows 8.1.

Utilizzo continuo di <iframe> per il contenuto remoto sarà necessaria una nuova voce in ApplicationContentUriRules per l'app. Le app con WebView richiedono nuove voci in ApplicationContentUriRules se il contenuto Web deve richiamare window.external.notify per generare un [evento ScriptNotify.](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) Se non si dispone di Visual Studio, è possibile aggiornare il manifesto dell'app aggiungendo il codice XML seguente, inclusi i caratteri jolly per i sottodomini (ad esempio, https:// \* .microsoft.com):


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

 

 
