---
title: Debug del codice
description: Debug del codice
ms.assetid: 315bc692-86bc-481e-abe4-f35309807a58
keywords:
- Interfacce di Media Player Windows, debug del codice
- interfacce, debug del codice
- debug del codice per le interfacce
- Interfacce di Media Player Windows, registrazione
- interfacce, registrazione
- funzionalità di registrazione nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e2305020b945d90adc1a47387ab2a13a3536e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332031"
---
# <a name="debugging-code"></a><span data-ttu-id="d767f-109">Debug del codice</span><span class="sxs-lookup"><span data-stu-id="d767f-109">Debugging Code</span></span>

<span data-ttu-id="d767f-110">Spesso si desidera vedere cosa accade all'interno dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d767f-110">You often will want to see what is happening inside your skin.</span></span> <span data-ttu-id="d767f-111">Questa operazione può essere eseguita tramite un controllo di testo o tramite un file di log.</span><span class="sxs-lookup"><span data-stu-id="d767f-111">You can do this through a text control or through a log file.</span></span>

<span data-ttu-id="d767f-112">È possibile creare un elemento di **testo** e posizionarlo temporaneamente su una parte dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d767f-112">You can create a **TEXT** element and place it on a part of your skin temporarily.</span></span> <span data-ttu-id="d767f-113">Ad esempio, è possibile usare il codice seguente per creare l'elemento di **testo** :</span><span class="sxs-lookup"><span data-stu-id="d767f-113">For example, you could use the following code to create your **TEXT** element:</span></span>


```C++
<!-- debugging control -- remove later -->        
<TEXT
    id = "debug"
    foregroundColor = "white"
    backgroundColor = "black"
    value = "debug"
    top = "100"
    left = "50"
    height = "15"
    width = "100" 
    z-order = "5" />
<!-- end debugging control -->
```



<span data-ttu-id="d767f-114">Se, ad esempio, si desidera visualizzare la posizione corrente del contenuto multimediale digitale in Windows Media Player, è possibile utilizzare codice simile al seguente per visualizzare la posizione corrente nella casella di testo.</span><span class="sxs-lookup"><span data-stu-id="d767f-114">Then, for example, if you want to see the current position of the digital media content in Windows Media Player, you could use code similar to the following to display the current position in the text box.</span></span>


```C++
<PLAYER
    id = "myplayer">
    <CONTROLS
        id = "mycontrols"
        currentPosition_onchange="value=player.controls.currentPosition"/>
</PLAYER>

```



## <a name="to-write-debugging-information-to-a-log-file"></a><span data-ttu-id="d767f-115">Per scrivere le informazioni di debug in un file di log</span><span class="sxs-lookup"><span data-stu-id="d767f-115">To Write Debugging Information to a Log File</span></span>

<span data-ttu-id="d767f-116">Per abilitare o disabilitare il debug, modificare il valore della seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="d767f-116">To enable or disable debugging, change the value of the following registry key:</span></span>

<span data-ttu-id="d767f-117">**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Preferences \\ ScriptDebugging**</span><span class="sxs-lookup"><span data-stu-id="d767f-117">**HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\MediaPlayer\\Preferences\\ScriptDebugging**</span></span>

<span data-ttu-id="d767f-118">Quando si imposta il valore su 1, la registrazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="d767f-118">When you set the value to 1, logging is enabled.</span></span> <span data-ttu-id="d767f-119">Quando si imposta il valore su 0 (impostazione predefinita), la registrazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="d767f-119">When you set the value to 0 (the default), logging is disabled.</span></span>

<span data-ttu-id="d767f-120">Se la registrazione è abilitata, un file verrà inserito nel computer dell'utente nella stessa cartella dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d767f-120">If logging is enabled, a file will be placed on the user's computer in the same folder as the skin.</span></span> <span data-ttu-id="d767f-121">Il file verrà denominato "*filename* \_ 0 \_log.txt", dove *filename* è il nome del file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d767f-121">The file will be named "*filename*\_0\_log.txt", where *filename* is the name of the skin file.</span></span> <span data-ttu-id="d767f-122">Il codice nell'interfaccia può scrivere testo in questo file usando il *tema*. metodo **logString** .</span><span class="sxs-lookup"><span data-stu-id="d767f-122">The code in your skin can write text to this file by using the *Theme*.**logString** method.</span></span> <span data-ttu-id="d767f-123">Questo può essere utile se si desidera determinare cosa accade all'interno del codice mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d767f-123">This can be useful if you want to determine what is going on inside your code while it is running.</span></span> <span data-ttu-id="d767f-124">Si noti che il file di testo è codificato con caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="d767f-124">Note that the text file is encoded with Unicode characters.</span></span>

<span data-ttu-id="d767f-125">Quando la registrazione è abilitata ed è stato installato un sistema di sviluppo che fornisce funzionalità di debug (ad esempio Microsoft Visual Studio), le eccezioni non gestite dal codice di script comporteranno l'apertura di una finestra di dialogo di avviso del debugger per ogni eccezione.</span><span class="sxs-lookup"><span data-stu-id="d767f-125">When logging is enabled and you have installed a development system that provides debugging capabilities (such as Microsoft Visual Studio), exceptions that are not handled by your script code will cause a debugger warning dialog box to open for each exception.</span></span> <span data-ttu-id="d767f-126">Si tratta di una funzionalità utile che consente di eseguire il debug del codice di script.</span><span class="sxs-lookup"><span data-stu-id="d767f-126">This is a useful feature to help you debug your script code.</span></span> <span data-ttu-id="d767f-127">Inoltre, è possibile alleghi manualmente il processo di Media Player Windows al debugger quando è abilitata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="d767f-127">Also, you can manually attach the Windows Media Player process to your debugger when logging is enabled.</span></span>

<span data-ttu-id="d767f-128">Questo SDK include un'interfaccia di esempio, denominata "registrazione", che illustra la funzionalità di registrazione nelle interfacce.</span><span class="sxs-lookup"><span data-stu-id="d767f-128">This SDK includes a sample skin, called "logging", that demonstrates logging functionality in skins.</span></span> <span data-ttu-id="d767f-129">Per ulteriori informazioni sull'utilizzo degli esempi, vedere [esempi](samples.md).</span><span class="sxs-lookup"><span data-stu-id="d767f-129">To learn more about using the samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d767f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d767f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d767f-131">**Informazioni sulle interfacce**</span><span class="sxs-lookup"><span data-stu-id="d767f-131">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




