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
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955167"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="899ab-103">Scrittura di uno script per configurare la directory virtuale</span><span class="sxs-lookup"><span data-stu-id="899ab-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="899ab-104">Per caricare un file nel server, è possibile utilizzare i valori predefiniti della proprietà IIS BITS.</span><span class="sxs-lookup"><span data-stu-id="899ab-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="899ab-105">Il file di caricamento viene scritto nell'URL come specificato nel nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="899ab-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="899ab-106">Per caricare il file in un'applicazione server e ricevere una risposta, modificare la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) per inviare i dati per riferimento (Invia il nome del file che contiene i dati) o per valore (Invia i dati nel corpo della richiesta).</span><span class="sxs-lookup"><span data-stu-id="899ab-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="899ab-107">Per un elenco e una descrizione delle proprietà che è possibile modificare, vedere [proprietà dell'estensione IIS BITS](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="899ab-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="899ab-108">Usare i metodi dell'interfaccia [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) per abilitare e disabilitare la directory virtuale per i caricamenti.</span><span class="sxs-lookup"><span data-stu-id="899ab-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="899ab-109">Nell'esempio seguente viene illustrato come utilizzare Windows script host per creare, configurare e abilitare una directory virtuale IIS per i caricamenti BITS.</span><span class="sxs-lookup"><span data-stu-id="899ab-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


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



<span data-ttu-id="899ab-110">Per modificare l'esempio precedente in modo da caricare i dati in un'applicazione server, aggiungere il codice seguente prima di **SetInfo**.</span><span class="sxs-lookup"><span data-stu-id="899ab-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="899ab-111">Il percorso del file di caricamento viene passato all'applicazione server myasp. asp nell'intestazione BITS-request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="899ab-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="899ab-112">Per ricevere il file di caricamento nel corpo della richiesta, impostare la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) su 2.</span><span class="sxs-lookup"><span data-stu-id="899ab-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="899ab-113">Per informazioni sulla ricezione dei dati di caricamento nell'applicazione server, vedere [uso delle intestazioni di richiesta/risposta per le notifiche BITS](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="899ab-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




