---
title: Fornire la sicurezza del client RDP
description: Alcune proprietà dell'oggetto Desktop remoto controllo ActiveX sono limitate a specifiche aree di sicurezza URL di Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710186"
---
# <a name="providing-for-rdp-client-security"></a>Fornire la sicurezza del client RDP

Per consentire ai client di proteggersi da server potenzialmente non attendibili, alcune proprietà dell'oggetto controllo Desktop remoto ActiveX sono limitate a aree di sicurezza URL Internet Explorer specifiche. Ciò significa che, quando un utente che visita il Web accede alla pagina e la pagina si trova in un'area di sicurezza con URL superiore rispetto al computer con cui si sta esplorando il Web, queste proprietà sono disabilitate. Queste proprietà limitate sono accessibili tramite l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) e l'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) e sono disponibili nelle aree di sicurezza URL Internet Explorer seguenti:

-   Risorse del computer
-   Intranet locale
-   Siti attendibili

Sono disabilitate in queste zone:

-   Internet
-   Siti con restrizioni

Se si chiamano queste proprietà limitate all'interno dell'applicazione Servizi Desktop remoto Web, è necessario chiamare [**IMsTscAx:: Get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx:: Get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) per accedere alle proprietà delle impostazioni protette.

Di seguito sono riportate le proprietà limitate a cui accede l'interfaccia **IMsTscSecuredSettings** :

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Questa proprietà specifica il programma che verrà avviato alla connessione.
-   [**Workdir**](imstscsecuredsettings-workdir.md). Questa proprietà specifica la directory di lavoro del programma specificato in [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   A [**schermo intero**](imstscsecuredsettings-fullscreen.md). Questa proprietà specifica se lo stato del controllo alla connessione sarà in modalità schermo intero o finestra. Se il valore di questa proprietà è **true**, la connessione verrà aperta in modalità schermo intero. Sebbene l'utilizzo della proprietà **FullScreen** sia limitato alle zone di sicurezza URL di Internet Explorer elencate in precedenza, un utente può sempre passare alla modalità schermo intero dopo la connessione premendo la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).

Di seguito sono riportate le proprietà a cui accede l'interfaccia **IMsRdpClientSecuredSettings** :

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Questa proprietà specifica se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Questa proprietà specifica come e quando applicare le combinazioni di tasti di Windows; ad esempio ALT + TAB.

Lo script seguente avvia Microsoft Notepad.exe al momento della connessione. Eseguire questo script prima di chiamare il metodo [**IMsTscAx:: Connect**](imstscax-connect.md) .

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




