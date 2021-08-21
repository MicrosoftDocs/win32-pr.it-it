---
title: Uso del Desktop remoto ActiveX con canali virtuali
description: Se è stata abilitata un'applicazione di canali virtuali nella distribuzione Servizi Desktop remoto, è possibile renderla disponibile per i computer client.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dae33c059a84422788bc49d47f95e0011f78930054ed3884669e8f35763461b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868731"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Uso del Desktop remoto ActiveX con canali virtuali

Se è stata abilitata un'applicazione di canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile renderla disponibile per i computer client che accedono al server Host sessione Desktop remoto (Host sessione Desktop remoto) tramite il controllo Desktop remoto ActiveX.

**Per rendere disponibile un'applicazione del canale virtuale**

1.  Distribuire il modulo lato server dell'applicazione e assicurarsi che sia in esecuzione nel server Host sessione Desktop remoto. Nella pagina di connessione dell'applicazione Web Servizi Desktop remoto in esecuzione nel server Web accedere alla proprietà **PluginDlls** [**dell'interfaccia IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) per specificare il nome della DLL del canale virtuale. Se sono presenti più plug-in, specificare un elenco delimitato da virgole di nomi di DLL. Ad esempio, se il plug-in del canale virtuale è denominato "MyPlugin.dll", usare il codice seguente:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Usare il codice seguente se si dispone di due DLL del canale virtuale. In questo esempio i nomi dei file DLL sono "MyPlugin.dll" e "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Per motivi di sicurezza, **la proprietà PluginDlls** accetta solo un elenco denominato di DLL del canale virtuale. Il controllo restituisce un errore se viene specificato un file system o un percorso UNC. Inoltre, i nomi delle DLL devono contenere solo caratteri alfanumerici.

2.  Assicurarsi che il modulo lato client sia installato nella directory %windir% \\ system32.

L'API del canale virtuale non consente il caricamento di più istanze della stessa DLL del canale virtuale all'interno di un singolo processo. Per questo problema, se sono presenti più istanze del controllo Desktop remoto ActiveX in esecuzione all'interno dello stesso processo, solo la prima istanza del controllo sarà in grado di caricare la DLL del canale virtuale. Se si progetta un'applicazione di canale virtuale che deve supportare [](dynamic-virtual-channels.md) più istanze all'interno di un singolo processo, è necessario usare l'API Canali virtuali dinamici per implementare l'applicazione del canale virtuale.

> [!Note]  
> Per impostazione predefinita, il Desktop remoto ActiveX carica le DLL client del canale virtuale dalla directory %windir% \\ system32. È possibile per un amministratore modificare questa directory DLL del plug-in client predefinito. A tale scopo, modificare la chiave del Registro di sistema **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** nel computer client. Questo percorso di directory non può essere specificato nel formato UNC.

 

 

 




