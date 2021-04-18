---
title: Registrazione del plug-in DVC
description: Viene descritta la sintassi per la voce del plug-in Dynamic Virtual Channel (DVC) per il client Connessione Desktop remoto (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300298"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="9ff5e-103">Registrazione del plug-in DVC</span><span class="sxs-lookup"><span data-stu-id="9ff5e-103">DVC plug-in registration</span></span>

<span data-ttu-id="9ff5e-104">Il plug-in Dynamic Virtual Channel (DVC) è registrato per l'utilizzo da parte del client di Connessione Desktop remoto (RDC) utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ff5e-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="9ff5e-105">Viene richiamato il metodo [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) del controllo ActiveX Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="9ff5e-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="9ff5e-106">Più voci devono essere separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="9ff5e-107">Scrittura della voce di plug-in nel seguente percorso del registro di sistema nel computer in cui viene avviato il processo client di Connessione Desktop remoto (RDC):</span><span class="sxs-lookup"><span data-stu-id="9ff5e-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="9ff5e-108">**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Terminal Server** il \\  \\  \\ ***nome del plug-in componenti aggiuntivi predefiniti del*** client Microsoft</span><span class="sxs-lookup"><span data-stu-id="9ff5e-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="9ff5e-109">È necessario creare la sottochiave *univoca del nome del plug-in* se non esiste.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="9ff5e-110">Il nome della sottochiave del *nome del plug-in univoco* è una stringa arbitraria che può identificare il plug-in.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="9ff5e-111">La stringa può essere costituita da qualsiasi combinazione di caratteri.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="9ff5e-112">In *nome plug-in univoco* è necessario aggiungere una voce che identifichi il plug-in.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="9ff5e-113">Nome voce = **nome**</span><span class="sxs-lookup"><span data-stu-id="9ff5e-113">Entry name = **Name**</span></span>

    <span data-ttu-id="9ff5e-114">Tipo di dati = **reg \_ SZ** o **reg \_ expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="9ff5e-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="9ff5e-115">In entrambi i casi, il valore della voce deve essere conforme a uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ff5e-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="9ff5e-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*: {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="9ff5e-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="9ff5e-117">Il plug-in non è necessariamente registrato nel registro di sistema di Windows come oggetto Component Object Model (COM), ma la DLL viene implementata come oggetto COM in-process.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="9ff5e-118">Il client RDC caricherà la DLL specificata da *plug-inDLLName* e recupererà l'oggetto com direttamente usando *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="9ff5e-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span><span class="sxs-lookup"><span data-stu-id="9ff5e-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="9ff5e-120">La DLL implementa la funzione [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) e la Esporta in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="9ff5e-121">Il client RDC utilizzerà la funzione **VirtualChannelGetInstance** per ottenere i puntatori dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="9ff5e-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="9ff5e-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="9ff5e-123">Il client RDC creerà un'istanza del plug-in come un normale oggetto COM utilizzando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con il *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="9ff5e-124">Il *plug-inDLLName* rappresenta il percorso completo e il nome file del file con estensione dll.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="9ff5e-125">Se il tipo di dati è **reg \_ expand \_ SZ**, il percorso può contenere variabili di ambiente non espanse che vengono espanse in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="9ff5e-126">Al termine dell'inizializzazione, il client di Connessione Desktop remoto (RDC) eseguirà le operazioni seguenti per ogni plug-in registrato:</span><span class="sxs-lookup"><span data-stu-id="9ff5e-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="9ff5e-127">Ottenere un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per ogni plug-in utilizzando uno dei metodi descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="9ff5e-128">Chiamare il metodo [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) di ogni interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .</span><span class="sxs-lookup"><span data-stu-id="9ff5e-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="9ff5e-129">Se il client si connette più volte allo stesso o a un server diverso, è possibile che siano presenti più chiamate ai metodi [**connessi**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) e [**disconnessi**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .</span><span class="sxs-lookup"><span data-stu-id="9ff5e-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="9ff5e-130">L'ultima chiamata che il plug-in deve gestire viene [**terminata**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="9ff5e-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="9ff5e-131">È un segnale che il client di Connessione Desktop remoto (RDC) sta per scaricare il plug-in.</span><span class="sxs-lookup"><span data-stu-id="9ff5e-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 