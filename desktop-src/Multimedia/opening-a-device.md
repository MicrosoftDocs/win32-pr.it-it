---
title: Apertura di un dispositivo
description: Apertura di un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Comando MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046593"
---
# <a name="opening-a-device"></a><span data-ttu-id="f93a8-104">Apertura di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="f93a8-104">Opening a Device</span></span>

<span data-ttu-id="f93a8-105">Prima di usare un dispositivo, è necessario inizializzarlo usando il comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="f93a8-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="f93a8-106">Questo comando carica il driver in memoria (se non è già caricato) e recupera l'identificatore del dispositivo che verrà usato per identificare il dispositivo nei successivi comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="f93a8-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="f93a8-107">È necessario controllare il valore restituito della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) prima di usare un nuovo identificatore di dispositivo per assicurarsi che l'identificatore sia valido.</span><span class="sxs-lookup"><span data-stu-id="f93a8-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="f93a8-108">È anche possibile recuperare un identificatore di dispositivo tramite la funzione [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f93a8-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="f93a8-109">Come tutti i messaggi di comando MCI, **MCI \_ Open** ha una struttura associata.</span><span class="sxs-lookup"><span data-stu-id="f93a8-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="f93a8-110">Queste strutture sono talvolta denominate *blocchi di parametri*.</span><span class="sxs-lookup"><span data-stu-id="f93a8-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="f93a8-111">La struttura predefinita per **MCI \_ Open** è [**MCI \_ Open \_ parametri**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="f93a8-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="f93a8-112">Alcuni dispositivi, ad esempio la *forma d'onda* e la *sovrapposizione*, hanno strutture estese, ad esempio [**MCI \_ Wave \_ Open \_ parametri**](mci-wave-open-parms.md) e [**MCI \_ OVLY \_ Open \_ parametri**](mci-ovly-open-parms.md), per contenere parametri facoltativi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="f93a8-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="f93a8-113">A meno che non sia necessario usare questi parametri aggiuntivi, è possibile usare la struttura **MCI \_ Open \_ parametri** con qualsiasi dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="f93a8-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="f93a8-114">Il numero di dispositivi che è possibile aprire è limitato solo dalla quantità di memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="f93a8-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="f93a8-115">Uso di un alias</span><span class="sxs-lookup"><span data-stu-id="f93a8-115">Using an Alias</span></span>

<span data-ttu-id="f93a8-116">Quando si apre un dispositivo, è possibile usare il flag "alias" per specificare un identificatore del dispositivo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="f93a8-117">Questo flag consente di assegnare un breve identificatore di dispositivo per i dispositivi composti con nomi di file lunghi e consente di aprire più istanze dello stesso file o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="f93a8-118">Ad esempio, il comando seguente assegna l'identificatore di dispositivo "birdcall" al nome file di lunghezza C: \\ NABIRDS \\ suoni \\ MOCKMTNG. WAV</span><span class="sxs-lookup"><span data-stu-id="f93a8-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="f93a8-119">Nell'interfaccia del messaggio di comando è possibile specificare un alias usando il membro **lpstrAlias** della struttura [**\_ \_ parametri aperta di MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f93a8-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="f93a8-120">Specifica di un tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="f93a8-120">Specifying a Device Type</span></span>

<span data-ttu-id="f93a8-121">Quando si apre un dispositivo, è possibile usare il flag "Type" per fare riferimento a un tipo di dispositivo, anziché a un driver di dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="f93a8-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="f93a8-122">Nell'esempio seguente viene aperto il file Waveform-Audio file C: \\ Windows \\ Chimes. WAV (usando il flag "Type" per specificare il tipo di dispositivo **WaveAudio** ) e assegna l'alias "Chimes":</span><span class="sxs-lookup"><span data-stu-id="f93a8-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="f93a8-123">Nell'interfaccia del messaggio di comando, la funzionalità del flag "Type" viene fornita dal membro **lpstrDeviceType** della struttura [**\_ \_ parametri aperta di MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f93a8-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="f93a8-124">Dispositivi semplici e composti</span><span class="sxs-lookup"><span data-stu-id="f93a8-124">Simple and Compound Devices</span></span>

<span data-ttu-id="f93a8-125">MCI classifica i driver di dispositivo come *composti* o *semplici*.</span><span class="sxs-lookup"><span data-stu-id="f93a8-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="f93a8-126">I driver per i dispositivi composti richiedono il nome di un file di dati per la riproduzione. i driver per i dispositivi semplici non lo sono.</span><span class="sxs-lookup"><span data-stu-id="f93a8-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="f93a8-127">I dispositivi semplici includono i dispositivi **CDAudio** e **videodisco** .</span><span class="sxs-lookup"><span data-stu-id="f93a8-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="f93a8-128">Esistono due modi per aprire i dispositivi semplici:</span><span class="sxs-lookup"><span data-stu-id="f93a8-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="f93a8-129">Specificare un puntatore a una stringa con terminazione null contenente il nome del dispositivo dal registro di sistema o dal file di SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="f93a8-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="f93a8-130">Ad esempio, è possibile aprire un dispositivo **videodisco** usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f93a8-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="f93a8-131">In questo caso, "videodisco" è il nome del dispositivo dal registro di sistema o dalla \[ \] sezione mci del SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="f93a8-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="f93a8-132">Specificare il nome effettivo del driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="f93a8-133">L'apertura di un dispositivo con il nome file del driver di dispositivo, tuttavia, rende l'applicazione specifica del dispositivo e può impedire l'esecuzione dell'applicazione in caso di modifica della configurazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="f93a8-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="f93a8-134">Se si usa un nome di file, non è necessario specificare il percorso completo o l'estensione del nome file. MCI presuppone che i driver si trovino in una directory di sistema e dispongano di. Estensione DRV filename.</span><span class="sxs-lookup"><span data-stu-id="f93a8-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="f93a8-135">I dispositivi composti includono i dispositivi **WaveAudio** e **sequencer** .</span><span class="sxs-lookup"><span data-stu-id="f93a8-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="f93a8-136">I dati per un dispositivo composto vengono talvolta definiti *elementi del dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="f93a8-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="f93a8-137">Questo documento, tuttavia, in genere fa riferimento a questi dati come file, anche se in alcuni casi i dati potrebbero non essere archiviati come file.</span><span class="sxs-lookup"><span data-stu-id="f93a8-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="f93a8-138">Sono disponibili tre modi per aprire un dispositivo composto:</span><span class="sxs-lookup"><span data-stu-id="f93a8-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="f93a8-139">Specificare solo il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-139">Specify only the device name.</span></span> <span data-ttu-id="f93a8-140">In questo modo è possibile aprire un dispositivo composto senza associare un nome di file.</span><span class="sxs-lookup"><span data-stu-id="f93a8-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="f93a8-141">La maggior parte dei dispositivi composti elabora solo i comandi [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) quando vengono aperti in questo modo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="f93a8-142">Specificare solo il nome del file.</span><span class="sxs-lookup"><span data-stu-id="f93a8-142">Specify only the filename.</span></span> <span data-ttu-id="f93a8-143">Il nome del dispositivo è determinato dalle associazioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f93a8-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="f93a8-144">Specificare il nome del file e il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-144">Specify the filename and the device name.</span></span> <span data-ttu-id="f93a8-145">MCI ignora le voci nel registro di sistema e apre il nome del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f93a8-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="f93a8-146">Per associare un file di dati a un dispositivo specifico, è possibile specificare il nome file e il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="f93a8-147">Il comando seguente, ad esempio, apre il dispositivo **WaveAudio** con il nome file. SND</span><span class="sxs-lookup"><span data-stu-id="f93a8-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="f93a8-148">Nell'interfaccia della stringa di comando è inoltre possibile abbreviare la specifica del nome del dispositivo utilizzando il formato punto esclamativo alternativo, come documentato con il comando [**Apri**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="f93a8-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="f93a8-149">Apertura di un dispositivo usando l'estensione filename</span><span class="sxs-lookup"><span data-stu-id="f93a8-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="f93a8-150">Se il comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)) specifica solo il nome del file, MCI usa l'estensione del nome file per selezionare il dispositivo appropriato nell'elenco nel registro di sistema o nella \[ sezione estensioni MCI \] del file SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="f93a8-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="f93a8-151">Le voci nella \[ sezione estensioni MCI \] usano il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="f93a8-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="f93a8-152">*\_*  =  *\_ nome del dispositivo* di estensione del nome file</span><span class="sxs-lookup"><span data-stu-id="f93a8-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="f93a8-153">MCI utilizza in modo implicito il *\_ nome del dispositivo* se l'estensione viene trovata e se non è stato specificato un nome di dispositivo nel comando **Apri** .</span><span class="sxs-lookup"><span data-stu-id="f93a8-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="f93a8-154">Nell'esempio seguente viene illustrata una \[ sezione delle estensioni MCI tipiche \] :</span><span class="sxs-lookup"><span data-stu-id="f93a8-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="f93a8-155">Usando queste definizioni, MCI apre il dispositivo **WaveAudio** se viene eseguito il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f93a8-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="f93a8-156">Nuovi file di dati</span><span class="sxs-lookup"><span data-stu-id="f93a8-156">New Data Files</span></span>

<span data-ttu-id="f93a8-157">Per creare un nuovo file di dati, è sufficiente specificare un nome file vuoto.</span><span class="sxs-lookup"><span data-stu-id="f93a8-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="f93a8-158">MCI non salva un nuovo file fino a quando non lo si salva usando il comando [**Save**](save.md) ([**MCI \_ Save**](mci-save.md)).</span><span class="sxs-lookup"><span data-stu-id="f93a8-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="f93a8-159">Quando si crea un nuovo file, è necessario includere un alias del dispositivo con il comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="f93a8-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="f93a8-160">Nell'esempio seguente viene aperto un nuovo file **WaveAudio** , viene avviata e arrestata la registrazione, quindi il file viene salvato e chiuso:</span><span class="sxs-lookup"><span data-stu-id="f93a8-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="f93a8-161">Dispositivi condivisibili</span><span class="sxs-lookup"><span data-stu-id="f93a8-161">Sharable Devices</span></span>

<span data-ttu-id="f93a8-162">Il flag "condivisibile" (MCI \_ aperto) \_ del comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)) consente a più applicazioni di accedere simultaneamente allo stesso dispositivo (o file) e all'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="f93a8-163">Se l'applicazione apre un dispositivo o un file come condivisibile, anche altre applicazioni possono accedervi aprendolo come condivisibile.</span><span class="sxs-lookup"><span data-stu-id="f93a8-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="f93a8-164">Il file o il dispositivo condiviso fornisce a ogni applicazione la possibilità di modificare i parametri che ne controllano lo stato operativo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="f93a8-165">Ogni volta che un dispositivo o un file viene aperto come condivisibile, MCI restituisce un identificatore univoco del dispositivo, anche se gli identificatori fanno riferimento alla stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="f93a8-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="f93a8-166">Se l'applicazione apre un dispositivo o un file senza specificarne lo stato condivisibile, nessun'altra applicazione potrà accedervi fino a quando l'applicazione non la chiude.</span><span class="sxs-lookup"><span data-stu-id="f93a8-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="f93a8-167">Inoltre, se un dispositivo supporta solo un'istanza aperta, il comando **Apri** avrà esito negativo se si specifica il flag condivisibile.</span><span class="sxs-lookup"><span data-stu-id="f93a8-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="f93a8-168">Se l'applicazione apre un dispositivo e specifica che è condivisibile, l'applicazione non deve fare supposizioni sullo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="f93a8-169">L'applicazione potrebbe dover compensare le modifiche apportate da altre applicazioni che accedono al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="f93a8-170">La maggior parte dei file composti non è condivisibile. Tuttavia, è possibile aprire più file oppure è possibile aprire più volte un singolo file.</span><span class="sxs-lookup"><span data-stu-id="f93a8-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="f93a8-171">Se si apre un singolo file più volte, MCI crea un'istanza indipendente per ogni istanza con uno stato operativo univoco.</span><span class="sxs-lookup"><span data-stu-id="f93a8-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="f93a8-172">Se si aprono più istanze di un file, è necessario assegnare a ognuno un identificatore univoco del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f93a8-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="f93a8-173">È possibile usare un alias, come descritto nella sezione seguente, per assegnare un nome univoco per ogni file.</span><span class="sxs-lookup"><span data-stu-id="f93a8-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 