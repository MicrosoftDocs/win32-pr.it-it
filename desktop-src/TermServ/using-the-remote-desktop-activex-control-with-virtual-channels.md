---
title: Uso del controllo ActiveX Desktop remoto con i canali virtuali
description: Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile questa applicazione per i computer client.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856289"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Uso del controllo ActiveX Desktop remoto con i canali virtuali

Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile questa applicazione ai computer client che accedono al server di host sessione Desktop remoto (host sessione Desktop remoto) tramite il Desktop remoto controllo ActiveX.

**Per rendere disponibile un'applicazione di canale virtuale**

1.  Distribuire il modulo lato server dell'applicazione e assicurarsi che sia in esecuzione nel server Host sessione Desktop remoto. Nella pagina connessione del Servizi Desktop remoto applicazione Web in esecuzione nel server Web, accedere alla proprietà **PluginDlls** dell'interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) per specificare il nome della dll del canale virtuale. Se si dispone di più di un plug-in, specificare un elenco delimitato da virgole di nomi di DLL. Ad esempio, se il plug-in del canale virtuale è denominato "MyPlugin.dll", usare il codice seguente:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Se si dispone di due dll di canale virtuale, utilizzare il codice seguente. In questo esempio i nomi dei file DLL sono "MyPlugin.dll" e "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Per motivi di sicurezza, la proprietà **PluginDlls** accetta solo un elenco denominato di dll del canale virtuale. Il controllo restituisce un errore se viene specificata una qualsiasi forma di file system o percorso UNC. Inoltre, i nomi delle dll devono contenere solo caratteri alfanumerici.

2.  Verificare che il modulo lato client sia installato nella directory% windir% \\ system32.

L'API del canale virtuale non consente il caricamento di più istanze della stessa DLL di canale virtuale all'interno di un singolo processo. Per questo motivo, se sono presenti più istanze del Desktop remoto controllo ActiveX in esecuzione all'interno dello stesso processo, solo la prima istanza del controllo sarà in grado di caricare la DLL del canale virtuale. Se si progetta un'applicazione di canale virtuale che deve supportare più istanze all'interno di un singolo processo, è necessario usare l'API dei [canali virtuali dinamici](dynamic-virtual-channels.md) per implementare l'applicazione del canale virtuale.

> [!Note]  
> Per impostazione predefinita, il controllo ActiveX Desktop remoto carica le dll client del canale virtuale dalla directory% windir% \\ system32. È possibile che un amministratore modifichi questa directory DLL del plug-in client predefinito. A tale scopo, modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server client** \\ **vdllpath** nel computer client. Impossibile specificare il percorso di directory nel formato UNC.

 

 

 




