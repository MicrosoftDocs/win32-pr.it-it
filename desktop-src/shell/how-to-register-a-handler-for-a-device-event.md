---
description: Descrive i processi per l'implementazione dei gestori di eventi del dispositivo nel registro di sistema.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Come registrare un gestore per un evento del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881562"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="e43a6-103">Come registrare un gestore per un evento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e43a6-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="e43a6-104">I gestori definiscono la parte software di AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="e43a6-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="e43a6-105">Definiscono l'icona e il nome descrittivo del software, nonché il componente Component Object Model (COM) per creare un'istanza di e come inizializzare il componente in risposta a un evento.</span><span class="sxs-lookup"><span data-stu-id="e43a6-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="e43a6-106">Ogni gestore per un evento specifico viene registrato come valore nella chiave **EventHandler** appropriata.</span><span class="sxs-lookup"><span data-stu-id="e43a6-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="e43a6-107">Quando viene rilevato l'evento, all'utente viene richiesto di scegliere un gestore da un elenco di tutti i gestori registrati per tale evento.</span><span class="sxs-lookup"><span data-stu-id="e43a6-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="e43a6-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="e43a6-108">Instructions</span></span>


<span data-ttu-id="e43a6-109">I gestori e i relativi valori associati sono definiti sotto la chiave dei \\ **gestori** AutoplayHandlers.</span><span class="sxs-lookup"><span data-stu-id="e43a6-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="e43a6-110">Le sottochiavi variano a seconda che il sistema sia in grado di leggere direttamente il contenuto del dispositivo o se il dispositivo fornisce contenuto al sistema tramite un'interfaccia proprietaria.</span><span class="sxs-lookup"><span data-stu-id="e43a6-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="e43a6-111">Nell'esempio seguente vengono illustrate le sottochiavi e i valori utilizzati per un dispositivo, ad esempio una videocamera digitale o un lettore MP3, che fornisce il contenuto al sistema tramite un'interfaccia proprietaria.</span><span class="sxs-lookup"><span data-stu-id="e43a6-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="e43a6-112">Il gestore di esempio è denominato **DataHandler**.</span><span class="sxs-lookup"><span data-stu-id="e43a6-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="e43a6-113">Mentre l'esempio mostra sia un ProgID che un valore di identificatore di classe (CLSID), in pratica questi valori si escludono a vicenda, in modo che sia presente solo uno o l'altro.</span><span class="sxs-lookup"><span data-stu-id="e43a6-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="e43a6-114">Il valore ProgID è preferibile.</span><span class="sxs-lookup"><span data-stu-id="e43a6-114">The ProgID value is preferred.</span></span> <span data-ttu-id="e43a6-115">A seconda di quale viene usato, deve puntare a un componente COM che implementa l'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="e43a6-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="e43a6-116">È possibile immettere il valore dell'azione come valore letterale, ad esempio "Play Music", come illustrato in questo esempio, oppure come nome file con una stringa di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e43a6-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="e43a6-117">È anche possibile immettere il valore del provider come valore letterale o come nome file con una stringa di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e43a6-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="e43a6-118">AutoPlay combina il valore dell'azione e il valore del provider con la parola "using" per creare una didascalia intuitiva da visualizzare nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e43a6-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="e43a6-119">Nell'esempio la didascalia risultante è "Play Music using Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="e43a6-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="e43a6-120">Il valore DefaultIcon punta a un file con estensione ico o a una risorsa in un file binario.</span><span class="sxs-lookup"><span data-stu-id="e43a6-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="e43a6-121">Se il valore numerico che segue il nome del file binario è pari a zero o superiore, è il valore di indice dell'icona in tale file binario.</span><span class="sxs-lookup"><span data-stu-id="e43a6-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="e43a6-122">Se è un valore negativo, si tratta dell'ID risorsa dell'icona.</span><span class="sxs-lookup"><span data-stu-id="e43a6-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="e43a6-123">Sono consigliati valori di indice negativi.</span><span class="sxs-lookup"><span data-stu-id="e43a6-123">Negative index values are recommended.</span></span> <span data-ttu-id="e43a6-124">Non è necessario alcun valore nel caso di un file con estensione ico.</span><span class="sxs-lookup"><span data-stu-id="e43a6-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="e43a6-125">Si consiglia di usare le variabili di ambiente nel percorso.</span><span class="sxs-lookup"><span data-stu-id="e43a6-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="e43a6-126">Il valore InitCmdLine passa senza modifiche tramite il metodo [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) prima che vengano chiamati altri metodi.</span><span class="sxs-lookup"><span data-stu-id="e43a6-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="e43a6-127">Nell'esempio seguente vengono illustrate le sottochiavi e i valori utilizzati per un dispositivo che può essere letto direttamente, ad esempio un'unità CD-ROM o un altro disco rimovibile.</span><span class="sxs-lookup"><span data-stu-id="e43a6-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="e43a6-128">Anche in questo caso, il gestore di esempio è denominato **DataHandler**.</span><span class="sxs-lookup"><span data-stu-id="e43a6-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="e43a6-129">In questo esempio, i valori dell'azione e del provider vengono visualizzati come nome file con una stringa di risorsa invece che con valori letterali, ma le stringhe a cui fanno riferimento vengono utilizzate nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="e43a6-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="e43a6-130">Vengono combinati con la parola "using" per creare una didascalia descrittiva, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e43a6-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="e43a6-131">I valori InvokeProgID e InvokeVerb sostituiscono CLSID, InitCmdLine e ProgID.</span><span class="sxs-lookup"><span data-stu-id="e43a6-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="e43a6-132">I valori InvokeProgID e InvokeVerb corrispondono ai nomi di chiave presenti nella **\_ \_ radice delle classi HKEY**, come illustrato nella voce del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="e43a6-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="e43a6-133">Questo set di chiavi di esempio corrisponde all'esempio di gestore specifico descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e43a6-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="e43a6-134">La funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza il CLSID per implementare l'applicazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="e43a6-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="e43a6-135">Dopo aver definito il gestore in uno di questi due modi, è necessario registrarlo per un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="e43a6-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="e43a6-136">A tale scopo, è necessario fornire il nome del gestore come valore per la chiave di tale evento in **EventHandlers**.</span><span class="sxs-lookup"><span data-stu-id="e43a6-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="e43a6-137">Nell'esempio seguente viene illustrato come registrare il gestore di **gestione** per l'evento GenericVolumeArrival.</span><span class="sxs-lookup"><span data-stu-id="e43a6-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="e43a6-138">Non è stato assegnato alcun valore di dati.</span><span class="sxs-lookup"><span data-stu-id="e43a6-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="e43a6-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e43a6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e43a6-140">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="e43a6-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="e43a6-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="e43a6-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
