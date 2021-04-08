---
title: Aggiornamento di plug-in DSP esistenti
description: Aggiornamento di plug-in DSP esistenti
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Plug-in di Windows Media Player, elaborazione dei segnali digitali (DSP)
- plug-in, elaborazione di segnali digitali (DSP)
- plug-in per l'elaborazione di segnali digitali, aggiornamento
- Plug-in DSP, aggiornamento
- versioni di Windows Media Player, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723471"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="32703-108">Aggiornamento di plug-in DSP esistenti</span><span class="sxs-lookup"><span data-stu-id="32703-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="32703-109">I plug-in DSP creati prima del rilascio di Windows Media Player 11 SDK potrebbero non funzionare come previsto con Windows Media Player 11 in esecuzione in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32703-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="32703-110">Per assicurarsi che i clienti che eseguono Windows Media Player 11 in Windows Vista possano usare i plug-in, è necessario apportare alcune modifiche al codice del plug-in DSP, ricompilare il progetto e distribuire il plug-in aggiornato ai clienti.</span><span class="sxs-lookup"><span data-stu-id="32703-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="32703-111">I progetti creati utilizzando la versione più recente della creazione guidata plug-in di Windows Media Player conterranno gli aggiornamenti necessari.</span><span class="sxs-lookup"><span data-stu-id="32703-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="32703-112">Vedere [gli aggiornamenti alla procedura guidata plug-in DSP per Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="32703-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="32703-113">È consigliabile eseguire la procedura guidata per creare un nuovo progetto di esempio e quindi usare uno strumento come Windiff.exe, disponibile in Visual Studio, per esaminare le differenze tra il codice di esempio e il codice di produzione.</span><span class="sxs-lookup"><span data-stu-id="32703-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="32703-114">È necessario apportare tre modifiche principali a tutti i plug-in DSP esistenti:</span><span class="sxs-lookup"><span data-stu-id="32703-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="32703-115">Modificare il modo in cui viene registrato il plug-in.</span><span class="sxs-lookup"><span data-stu-id="32703-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="32703-116">Il plug-in esistente registra probabilmente il modello di threading come "Apartment".</span><span class="sxs-lookup"><span data-stu-id="32703-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="32703-117">Windows Media Player 11 in esecuzione su Windows Vista richiede che i plug-in DSP registrino il modello di threading come "both".</span><span class="sxs-lookup"><span data-stu-id="32703-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="32703-118">È possibile risolvere il problema modificando il valore del modello di threading nel file *NomeProgetto*. RGS, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="32703-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="32703-119">Se si specifica il modello di threading come "both", vengono rimosse tutte le serializzazioni fornite da COM per le chiamate alle interfacce personalizzate.</span><span class="sxs-lookup"><span data-stu-id="32703-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="32703-120">Se si effettuano chiamate alle interfacce personalizzate da più thread, è necessario fornire questa serializzazione manualmente.</span><span class="sxs-lookup"><span data-stu-id="32703-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="32703-121">Windows Media Player 11 garantisce che le chiamate alle interfacce DMO vengano serializzate correttamente.</span><span class="sxs-lookup"><span data-stu-id="32703-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="32703-122">Aggiungere chiamate a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuovo tipo di plug-in: WMP \_ plug- \_ DSP OUTOFPROC \_ in DllRegisterServer e DllUnregisterServer nel file *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="32703-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="32703-123">Per informazioni dettagliate, vedere le pagine di riferimento per questi metodi.</span><span class="sxs-lookup"><span data-stu-id="32703-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="32703-124">Creare e distribuire una DLL proxy/stub per abilitare il marshalling COM di qualsiasi interfaccia personalizzata implementata o creata dalla classe del plug-in.</span><span class="sxs-lookup"><span data-stu-id="32703-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="32703-125">Un'interfaccia personalizzata è un'interfaccia proprietaria che è possibile definire e implementare per l'utilizzo da parte dell'oggetto plug-in.</span><span class="sxs-lookup"><span data-stu-id="32703-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="32703-126">Questo include l'interfaccia personalizzata usata dalla pagina delle proprietà, se ne è stato fornito uno, ma potrebbe includere anche interfacce che si connettono ai plug-in dell'interfaccia utente, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="32703-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="32703-127">Un esempio di interfaccia personalizzata creata dalla procedura guidata plug-in è *Iprojectname*.</span><span class="sxs-lookup"><span data-stu-id="32703-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="32703-128">Esempi di interfacce che non sono interfacce personalizzate includono **IMediaObject** e **IWMPPluginEnable**.</span><span class="sxs-lookup"><span data-stu-id="32703-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="32703-129">Se il plug-in DSP elabora audio, è necessario aggiungere anche il supporto per i nuovi formati audio seguenti:</span><span class="sxs-lookup"><span data-stu-id="32703-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="32703-130">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="32703-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="32703-131">\_Formato Wave \_ estendibile con subformat KSDATAFORMAT \_ sottotipo \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="32703-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="32703-132">Se il plug-in DSP elabora video, è necessario aggiungere il supporto per il formato video NV12.</span><span class="sxs-lookup"><span data-stu-id="32703-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="32703-133">Vedere il plug-in di esempio audio o video DSP creato dalla procedura guidata per un esempio di come elaborare questi tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="32703-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="32703-134">Informazioni sul progetto proxy/stub</span><span class="sxs-lookup"><span data-stu-id="32703-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="32703-135">Probabilmente il modo più semplice per creare un progetto DLL proxy/stub per il plug-in DSP consiste nell'eseguire la procedura guidata plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="32703-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="32703-136">Verrà creato un progetto proxy/stub di esempio che è possibile modificare per usare il codice esistente.</span><span class="sxs-lookup"><span data-stu-id="32703-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="32703-137">Sarà necessario apportare le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="32703-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="32703-138">Rimuovere tutte le definizioni esistenti per le interfacce personalizzate dal codice.</span><span class="sxs-lookup"><span data-stu-id="32703-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="32703-139">Ad esempio, la procedura guidata plug-in DSP di Windows Media Player 10 SDK ha creato la definizione dell'interfaccia *Iprojectname* nel file *NomeProgetto*. h usando la parola chiave **Interface** .</span><span class="sxs-lookup"><span data-stu-id="32703-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="32703-140">Definire le interfacce personalizzate nel file IDL del progetto di proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="32703-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="32703-141">Compilare il progetto proxy/stub prima del progetto principale.</span><span class="sxs-lookup"><span data-stu-id="32703-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="32703-142">È possibile configurare Visual Studio in modo che esegua questa operazione automaticamente se entrambi i progetti fanno parte della stessa soluzione.</span><span class="sxs-lookup"><span data-stu-id="32703-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="32703-143">Il compilatore MIDL creerà un nuovo file di intestazione con un nome nel formato *NomeProgetto* \_ h.h.</span><span class="sxs-lookup"><span data-stu-id="32703-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="32703-144">È necessario includere questa intestazione nel progetto principale (in *NomeProgetto*. h).</span><span class="sxs-lookup"><span data-stu-id="32703-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="32703-145">Contiene le definizioni per le interfacce personalizzate.</span><span class="sxs-lookup"><span data-stu-id="32703-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="32703-146">Distribuzione del plug-in aggiornato</span><span class="sxs-lookup"><span data-stu-id="32703-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="32703-147">È possibile installare il plug-in aggiornato nei computer degli utenti esattamente come in passato.</span><span class="sxs-lookup"><span data-stu-id="32703-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="32703-148">Tuttavia, è ora necessario distribuire e registrare anche la DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="32703-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32703-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32703-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32703-150">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="32703-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




