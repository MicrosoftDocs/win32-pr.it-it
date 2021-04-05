---
title: comando Apri (Corecrt \_ io. h)
description: Il comando Apri Inizializza un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Apri comando Windows Multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741431"
---
# <a name="open-command"></a><span data-ttu-id="5fa4b-105">Apri comando</span><span class="sxs-lookup"><span data-stu-id="5fa4b-105">open command</span></span>

<span data-ttu-id="5fa4b-106">Il comando Apri Inizializza un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-106">The open command initializes a device.</span></span> <span data-ttu-id="5fa4b-107">Tutti i dispositivi MCI riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="5fa4b-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="5fa4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fa4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa4b-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="5fa4b-111">Identificatore di un dispositivo MCI o di un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="5fa4b-112">Può essere un nome di dispositivo (come indicato nel registro di sistema o il file di SYSTEM.INI) o il nome del file del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="5fa4b-113">Se si specifica il nome del file del driver di dispositivo, è possibile includere facoltativamente. Estensione DRV, ma è consigliabile non includere il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="5fa4b-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5fa4b-115">Flag che identifica gli elementi da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="5fa4b-116">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Apri** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="5fa4b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5fa4b-117">Value</span></span>        | <span data-ttu-id="5fa4b-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5fa4b-118">Meaning</span></span>                                                        | <span data-ttu-id="5fa4b-119">Significato</span><span class="sxs-lookup"><span data-stu-id="5fa4b-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5fa4b-120">cdaudio</span><span class="sxs-lookup"><span data-stu-id="5fa4b-120">cdaudio</span></span>      | <span data-ttu-id="5fa4b-121">alias del *dispositivo \_ alias* condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="5fa4b-122">Digitare *il \_ tipo di dispositivo*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="5fa4b-123">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="5fa4b-123">digitalvideo</span></span> | <span data-ttu-id="5fa4b-124">alias *Device \_ aliaselementname* Nostatic *HWND* padre condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="5fa4b-125">tipo *di tipo di \_* *dispositivo \_* stile di popup stile sovrapposto stile figlio stile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="5fa4b-126">overlay</span><span class="sxs-lookup"><span data-stu-id="5fa4b-126">overlay</span></span>      | <span data-ttu-id="5fa4b-127">alias *dispositivo \_* *alias padre* alias del dispositivo figlio stile condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="5fa4b-128">tipo di tipo di dispositivo *tipo \_ stile* di *popup \_* stile sovrapposto stile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="5fa4b-129">sequencer</span><span class="sxs-lookup"><span data-stu-id="5fa4b-129">sequencer</span></span>    | <span data-ttu-id="5fa4b-130">alias del *dispositivo \_ alias* condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="5fa4b-131">Digitare *il \_ tipo di dispositivo*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="5fa4b-132">VCR</span><span class="sxs-lookup"><span data-stu-id="5fa4b-132">vcr</span></span>          | <span data-ttu-id="5fa4b-133">alias del *dispositivo \_ alias* condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="5fa4b-134">Digitare *il \_ tipo di dispositivo*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="5fa4b-135">videodisk</span><span class="sxs-lookup"><span data-stu-id="5fa4b-135">videodisk</span></span>    | <span data-ttu-id="5fa4b-136">alias del *dispositivo \_ alias* condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="5fa4b-137">Digitare *il \_ tipo di dispositivo*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="5fa4b-138">WaveAudio</span><span class="sxs-lookup"><span data-stu-id="5fa4b-138">waveaudio</span></span>    | <span data-ttu-id="5fa4b-139">*\_ dimensioni del buffer* di alias del *dispositivo \_* alias</span><span class="sxs-lookup"><span data-stu-id="5fa4b-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="5fa4b-140">tipo di *dispositivo \_* condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="5fa4b-141">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszOpenFlags** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="5fa4b-142">Valore</span><span class="sxs-lookup"><span data-stu-id="5fa4b-142">Value</span></span>                 | <span data-ttu-id="5fa4b-143">Significato</span><span class="sxs-lookup"><span data-stu-id="5fa4b-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa4b-144">alias *dispositivo \_* alias</span><span class="sxs-lookup"><span data-stu-id="5fa4b-144">alias *device\_alias*</span></span> | <span data-ttu-id="5fa4b-145">Specifica un nome alternativo per il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="5fa4b-146">Se specificato, deve essere usato come ID del *dispositivo \_* nei comandi successivi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="5fa4b-147">*ElementName*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-147">*elementname*</span></span>         | <span data-ttu-id="5fa4b-148">Specifica il nome dell'elemento del dispositivo (file) caricato all'apertura del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5fa4b-149">*\_ dimensioni buffer* buffer</span><span class="sxs-lookup"><span data-stu-id="5fa4b-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="5fa4b-150">Imposta la dimensione, in secondi, del buffer utilizzato dal dispositivo Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="5fa4b-151">Le dimensioni predefinite del buffer vengono impostate quando il dispositivo Waveform-Audio è installato o configurato.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="5fa4b-152">In genere, le dimensioni del buffer sono impostate su 4 secondi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="5fa4b-153">Con il dispositivo MCIWAVE, le dimensioni minime sono pari a 2 secondi e le dimensioni massime sono di 9 secondi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="5fa4b-154">*HWND* padre</span><span class="sxs-lookup"><span data-stu-id="5fa4b-154">parent *hwnd*</span></span>         | <span data-ttu-id="5fa4b-155">Specifica l'handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5fa4b-156">condivisibile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-156">sharable</span></span>              | <span data-ttu-id="5fa4b-157">Inizializza il dispositivo o il file come condivisibile.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="5fa4b-158">I successivi tentativi di apertura del dispositivo o del file avranno esito negativo a meno che non si specifichi "condivisibile" sia nei comandi **aperti** originali che in quelli successivi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="5fa4b-159">MCI restituisce un errore di dispositivo non valido se il dispositivo è già aperto e non condivisibile.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="5fa4b-160">I dispositivi MCISEQ sequencer e MCIWAVE non supportano i file condivisi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="5fa4b-161">figlio stile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-161">style child</span></span>           | <span data-ttu-id="5fa4b-162">Apre una finestra con uno stile finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="5fa4b-163">stile sovrapposto</span><span class="sxs-lookup"><span data-stu-id="5fa4b-163">style overlapped</span></span>      | <span data-ttu-id="5fa4b-164">Apre una finestra con uno stile di finestra sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5fa4b-165">popup stile</span><span class="sxs-lookup"><span data-stu-id="5fa4b-165">style popup</span></span>           | <span data-ttu-id="5fa4b-166">Apre una finestra con uno stile finestra popup.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5fa4b-167">*\_ tipo stile*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-167">style *style\_type*</span></span>   | <span data-ttu-id="5fa4b-168">Indica uno stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="5fa4b-169">Digitare *il \_ tipo di dispositivo*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-169">type *device\_type*</span></span>   | <span data-ttu-id="5fa4b-170">Specifica il tipo di dispositivo di un file.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="5fa4b-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5fa4b-172">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="5fa4b-173">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5fa4b-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa4b-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fa4b-174">Return Value</span></span>

<span data-ttu-id="5fa4b-175">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa4b-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fa4b-176">Remarks</span></span>

<span data-ttu-id="5fa4b-177">MCI riserva "CDAudio" per il tipo di dispositivo audio CD "videodisco" per il tipo di dispositivo videodisco, "Sequencer" per il tipo di dispositivo MIDI sequencer, "AVIVideo" per il tipo di dispositivo Digital-video e "WaveAudio" per il tipo di dispositivo Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="5fa4b-178">In alternativa al flag "Type", MCI può selezionare il dispositivo in base all'estensione usata dal file, come registrato nel registro di sistema o nella \[ sezione relativa all'estensione MCI \] del file di SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="5fa4b-179">MCI può aprire i file AVI usando un puntatore a interfaccia di file o un puntatore a interfaccia di flusso.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="5fa4b-180">Per aprire un file usando entrambi i tipi di puntatore a interfaccia, specificare un simbolo di chiocciola (@) seguito dal puntatore a interfaccia al posto del nome del file o del dispositivo per il parametro *lpszDevice* .</span><span class="sxs-lookup"><span data-stu-id="5fa4b-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="5fa4b-181">Per ulteriori informazioni sulle interfacce di file e di flusso, vedere " [funzioni e macro di avifile](avifile-functions-and-macros.md)".</span><span class="sxs-lookup"><span data-stu-id="5fa4b-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="5fa4b-182">Il comando che segue apre il dispositivo "audio".</span><span class="sxs-lookup"><span data-stu-id="5fa4b-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="5fa4b-183">Con il nome del dispositivo "nuovo", il driver della forma d'onda prepara una nuova risorsa di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="5fa4b-184">Il comando assegna l'alias del dispositivo "audio" e specifica un buffer di 6 secondi.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="5fa4b-185">È possibile eliminare il flag "Type" Se si combina il nome del dispositivo con il nome file.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="5fa4b-186">MCI riconosce questa combinazione quando si usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="5fa4b-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="5fa4b-187">*\_ nome dispositivo* .</span><span class="sxs-lookup"><span data-stu-id="5fa4b-187">*device\_name* !</span></span> <span data-ttu-id="5fa4b-188">*\_nome elemento*</span><span class="sxs-lookup"><span data-stu-id="5fa4b-188">*element\_name*</span></span>

<span data-ttu-id="5fa4b-189">Il punto esclamativo separa il nome del dispositivo dal nome del file.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="5fa4b-190">Il punto esclamativo non deve essere delimitato da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="5fa4b-191">Nell'esempio seguente viene aperto il diritto. File WAV che usa il dispositivo "WaveAudio".</span><span class="sxs-lookup"><span data-stu-id="5fa4b-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="5fa4b-192">Il driver MCIWAVE richiede un dispositivo audio e una forma d'onda asincrona.</span><span class="sxs-lookup"><span data-stu-id="5fa4b-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa4b-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fa4b-193">Requirements</span></span>



| <span data-ttu-id="5fa4b-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa4b-194">Requirement</span></span> | <span data-ttu-id="5fa4b-195">Valore</span><span class="sxs-lookup"><span data-stu-id="5fa4b-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa4b-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fa4b-196">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa4b-197">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5fa4b-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5fa4b-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fa4b-198">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa4b-199">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5fa4b-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5fa4b-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fa4b-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fa4b-201"><dt>\_Io. h Corecrt</dt></span><span class="sxs-lookup"><span data-stu-id="5fa4b-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa4b-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fa4b-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa4b-203">MCI</span><span class="sxs-lookup"><span data-stu-id="5fa4b-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5fa4b-204">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="5fa4b-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

