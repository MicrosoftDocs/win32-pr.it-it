---
title: Scrittura di uno script per configurare la directory virtuale
description: Scrittura di uno script per configurare la directory virtuale
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004601"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Scrittura di uno script per configurare la directory virtuale

È possibile usare i valori predefiniti delle proprietà IIS BITS per caricare un file nel server. Il file di caricamento viene scritto nell'URL come specificato nel nome file remoto del processo. Per caricare il file in un'applicazione server e ricevere una risposta, modificare la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) per inviare i dati per riferimento (invia il nome del file che contiene i dati) o per valore (invia i dati nel corpo della richiesta).

Per un elenco e una descrizione delle proprietà che è possibile modificare, vedere Proprietà [dell'estensione IIS BITS](bits-iis-extension-properties.md). Usare i metodi [**dell'interfaccia IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) per abilitare e disabilitare la directory virtuale per i caricamenti.

L'esempio seguente illustra come usare Windows Script Host per creare, configurare e abilitare una directory virtuale IIS per i caricamenti BITS.


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



Per modificare l'esempio precedente per caricare i dati in un'applicazione server, aggiungere il codice seguente prima **di SetInfo**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



Il percorso del file di caricamento viene passato all'applicazione server myasp.asp nell'intestazione BITS-Request-DataFile-Name. Per ricevere il file di caricamento nel corpo della richiesta, impostare la [proprietà BITSServerNotificationType](bits-iis-extension-properties.md) su 2.

Per informazioni sulla ricezione dei dati di caricamento nell'applicazione server, vedere [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).

 

 




