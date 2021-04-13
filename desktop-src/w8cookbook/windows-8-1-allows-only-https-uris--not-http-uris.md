---
title: URI in Windows 8.1
description: Windows 8.1 consente solo URI https, non URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399565"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 consente solo URI https, non URI http

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

Mentre le app compilate per Windows 8 possono includere URI http e HTTPS negli URI del contenuto dell'applicazione, le app create per Windows 8.1 possono includere solo URI https.

L'unica eccezione è per ContentUriRules dinamici specificati nel file di AppxManifest.xml dell'app. Con ContentUriRules dinamici, le app possono accedere ad altri domini o risorse di rete forniti dall'amministratore, ad esempio gli URI Criteri di gruppo. Tuttavia, i ContentUriRules dinamici sono disponibili solo per le app di Windows Store se soddisfano le condizioni seguenti:

-   Il Criteri di gruppo è abilitato
-   Il pacchetto ha specificato la funzionalità enterpriseAuthentication
-   Il OSMaxVersionTested del pacchetto è Windows 8.1 o superiore

Le nuove limitazioni in Windows 8.1 fanno parte delle restrizioni di sicurezza avanzate per proteggere ulteriormente la piattaforma.

## <a name="manifestations"></a>Manifestazioni

Quando si esegue un'app compilata per Windows 8 in Windows 8.1, è consentito l'uso degli URI http nella [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .

## <a name="mitigations"></a>Soluzioni di prevenzione

È consigliabile che gli sviluppatori WWA passino da [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) al controllo [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-webview>). Tuttavia, se è necessario il supporto per AppCache, IndexedDB, la georilevazione o l'accesso agli Appunti a livello di codice, sarà necessario continuare a usare <iframe> per Windows 8.1.

Utilizzo continuo di <iframe> per il contenuto remoto è necessaria una nuova voce in ApplicationContentUriRules per l'app. Le app con WebView richiedono nuove voci in ApplicationContentUriRules se il contenuto Web deve richiamare Window. External. Notify per la generazione di un evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . Se non si dispone di Visual Studio, è possibile aggiornare il manifesto dell'applicazione aggiungendo il codice XML seguente, inclusi i caratteri jolly per i sottodomini, ad esempio https:// \* . Microsoft.com:


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
-   [<iframe>\| <iframe> oggetto elemento](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Classe WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [Evento WebView. ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 