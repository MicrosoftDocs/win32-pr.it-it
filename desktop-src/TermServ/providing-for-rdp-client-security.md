---
title: Garantire la sicurezza del client RDP
description: Alcune proprietà dell'oggetto Desktop remoto ActiveX sono limitate a specifiche aree Internet Explorer di sicurezza URL.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdcfbc2b26363ff7f13ed15b3486249aab804cd1bde418f60d71db918f25567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940615"
---
# <a name="providing-for-rdp-client-security"></a>Garantire la sicurezza del client RDP

Per consentire ai client di proteggersi da server potenzialmente non attendibili, alcune proprietà dell'oggetto controllo Desktop remoto ActiveX sono limitate Internet Explorer aree di sicurezza URL specifiche. Ciò significa che, quando un utente che esplora il Web accede alla pagina e la pagina si trova in un'area di sicurezza con URL superiore a quella del computer con cui esplora il Web, queste proprietà sono disabilitate. Queste proprietà con restrizioni sono accessibili tramite [**l'interfaccia IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e [**l'interfaccia IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e sono disponibili nelle aree di sicurezza url Internet Explorer seguenti:

-   Risorse del computer
-   Intranet locale
-   Siti attendibili

Sono disabilitati nelle zone seguenti:

-   Internet
-   Siti con restrizioni

Se si chiamano queste proprietà con restrizioni all'interno dell'applicazione Web Servizi Desktop remoto, è necessario chiamare [**IMsTscAx::get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx::get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) per accedere alle proprietà Impostazioni protette.

Le proprietà con restrizioni a cui accede **l'interfaccia IMsTscSecuredSettings** sono le seguenti:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Questa proprietà specifica il programma che verrà avviato al momento della connessione.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Questa proprietà specifica la directory di lavoro del programma specificato in [**StartProgram.**](imstscsecuredsettings-startprogram.md)
-   [**FullScreen**](imstscsecuredsettings-fullscreen.md). Questa proprietà specifica se lo stato del controllo al momento della connessione sarà in modalità schermo intero o finestra. Se il valore di questa proprietà è **TRUE,** la connessione verrà aperta in modalità schermo intero. Anche se l'uso della proprietà **FullScreen** è limitato alle aree di sicurezza URL di Internet Explorer elencate in precedenza, [](terminal-services-shortcut-keys.md) un utente può sempre passare alla modalità schermo intero dopo la connessione premendo la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL+ALT+INTERR).

Le proprietà a cui **accede l'interfaccia IMsRdpClientSecuredSettings** sono le seguenti:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Questa proprietà specifica se reindirizzare i suoni o riprodurre suoni Desktop remoto server Host sessione Desktop remoto.
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Questa proprietà specifica come e quando applicare Windows combinazioni di tasti; ad esempio ALT+TAB.

Lo script seguente avvia Microsoft Notepad.exe alla connessione. Eseguire questo script prima di chiamare [**il metodo IMsTscAx::Connessione.**](imstscax-connect.md)

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




