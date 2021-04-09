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
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="994f4-103">Uso del controllo ActiveX Desktop remoto con i canali virtuali</span><span class="sxs-lookup"><span data-stu-id="994f4-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="994f4-104">Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile questa applicazione ai computer client che accedono al server di host sessione Desktop remoto (host sessione Desktop remoto) tramite il Desktop remoto controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="994f4-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="994f4-105">**Per rendere disponibile un'applicazione di canale virtuale**</span><span class="sxs-lookup"><span data-stu-id="994f4-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="994f4-106">Distribuire il modulo lato server dell'applicazione e assicurarsi che sia in esecuzione nel server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="994f4-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="994f4-107">Nella pagina connessione del Servizi Desktop remoto applicazione Web in esecuzione nel server Web, accedere alla proprietà **PluginDlls** dell'interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) per specificare il nome della dll del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="994f4-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="994f4-108">Se si dispone di più di un plug-in, specificare un elenco delimitato da virgole di nomi di DLL.</span><span class="sxs-lookup"><span data-stu-id="994f4-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="994f4-109">Ad esempio, se il plug-in del canale virtuale è denominato "MyPlugin.dll", usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="994f4-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="994f4-110">Se si dispone di due dll di canale virtuale, utilizzare il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="994f4-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="994f4-111">In questo esempio i nomi dei file DLL sono "MyPlugin.dll" e "Vdriver.dll":</span><span class="sxs-lookup"><span data-stu-id="994f4-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="994f4-112">Per motivi di sicurezza, la proprietà **PluginDlls** accetta solo un elenco denominato di dll del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="994f4-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="994f4-113">Il controllo restituisce un errore se viene specificata una qualsiasi forma di file system o percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="994f4-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="994f4-114">Inoltre, i nomi delle dll devono contenere solo caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="994f4-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="994f4-115">Verificare che il modulo lato client sia installato nella directory% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="994f4-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="994f4-116">L'API del canale virtuale non consente il caricamento di più istanze della stessa DLL di canale virtuale all'interno di un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="994f4-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="994f4-117">Per questo motivo, se sono presenti più istanze del Desktop remoto controllo ActiveX in esecuzione all'interno dello stesso processo, solo la prima istanza del controllo sarà in grado di caricare la DLL del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="994f4-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="994f4-118">Se si progetta un'applicazione di canale virtuale che deve supportare più istanze all'interno di un singolo processo, è necessario usare l'API dei [canali virtuali dinamici](dynamic-virtual-channels.md) per implementare l'applicazione del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="994f4-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="994f4-119">Per impostazione predefinita, il controllo ActiveX Desktop remoto carica le dll client del canale virtuale dalla directory% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="994f4-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="994f4-120">È possibile che un amministratore modifichi questa directory DLL del plug-in client predefinito.</span><span class="sxs-lookup"><span data-stu-id="994f4-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="994f4-121">A tale scopo, modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server client** \\ **vdllpath** nel computer client.</span><span class="sxs-lookup"><span data-stu-id="994f4-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="994f4-122">Impossibile specificare il percorso di directory nel formato UNC.</span><span class="sxs-lookup"><span data-stu-id="994f4-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




