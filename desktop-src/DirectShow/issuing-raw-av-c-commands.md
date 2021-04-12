---
description: Emissione di comandi AV/C non elaborati
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emissione di comandi AV/C non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401155"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="7412e-103">Emissione di comandi AV/C non elaborati</span><span class="sxs-lookup"><span data-stu-id="7412e-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="7412e-104">Le interfacce [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funzionano traducendo le chiamate al metodo in comandi per il driver, interpretando quindi la risposta del driver e restituendo il valore tramite un **HRESULT** o un parametro di output.</span><span class="sxs-lookup"><span data-stu-id="7412e-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="7412e-105">Tuttavia, alcune funzioni del dispositivo potrebbero non essere accessibili tramite questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7412e-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="7412e-106">MSDV supporta quindi l'invio di comandi AV/C non elaborati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7412e-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="7412e-107">Quando si usa questa funzionalità, è necessario tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7412e-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="7412e-108">Il comando viene passato direttamente al dispositivo, senza il controllo degli errori o la convalida dei parametri.</span><span class="sxs-lookup"><span data-stu-id="7412e-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="7412e-109">Per questo motivo, è necessario emettere comandi AV/C non elaborati solo quando le interfacce DirectShow non implementano la funzionalità necessaria.</span><span class="sxs-lookup"><span data-stu-id="7412e-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="7412e-110">Tutti i comandi AV/C non elaborati sono sincroni.</span><span class="sxs-lookup"><span data-stu-id="7412e-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="7412e-111">Il thread che emette il comando si blocca fino a quando il comando non restituisce.</span><span class="sxs-lookup"><span data-stu-id="7412e-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="7412e-112">È possibile assegnare un solo comando alla volta.</span><span class="sxs-lookup"><span data-stu-id="7412e-112">Only one command can be given at a time.</span></span> <span data-ttu-id="7412e-113">Durante l'elaborazione del comando, il dispositivo rifiuterà qualsiasi comando aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="7412e-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="7412e-114">Il driver UVC non supporta i comandi AV/C non elaborati.</span><span class="sxs-lookup"><span data-stu-id="7412e-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="7412e-115">Per inviare un comando AV/C, formattare il comando come una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="7412e-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="7412e-116">Quindi, chiamare [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="7412e-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="7412e-117">Passare il flag ED \_ \_ ext \_ dev \_ , le dimensioni della matrice e la matrice.</span><span class="sxs-lookup"><span data-stu-id="7412e-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="7412e-118">È necessario eseguire il cast dell'indirizzo della matrice a un tipo \**LPOLESTR \** _, perché lo scopo originale di questo parametro è restituire un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="7412e-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="7412e-119">Il contenuto della matrice viene passato direttamente al dispositivo, quindi è necessario prestare attenzione a formattarlo correttamente.</span><span class="sxs-lookup"><span data-stu-id="7412e-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="7412e-120">Un comando può avere come destinazione l'unità (videocamera) o un'unità secondaria (nastro o fotocamera).</span><span class="sxs-lookup"><span data-stu-id="7412e-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="7412e-121">Gli standard pertinenti sono disponibili nel [sito Web di associazione commerciale 1394](https://1394ta.org).</span><span class="sxs-lookup"><span data-stu-id="7412e-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="7412e-122">Specifica generale del set di comandi dell'interfaccia digitale AV/C</span><span class="sxs-lookup"><span data-stu-id="7412e-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="7412e-123">Specifica di unità di registrazione/lettore nastri AV/C</span><span class="sxs-lookup"><span data-stu-id="7412e-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="7412e-124">Il primo descrive come formattare i comandi AV/C ed elenca i comandi di unità.</span><span class="sxs-lookup"><span data-stu-id="7412e-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="7412e-125">La seconda specifica elenca i comandi delle sottounità.</span><span class="sxs-lookup"><span data-stu-id="7412e-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="7412e-126">Il metodo **GetTransportBasicParameters** può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="7412e-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="7412e-127">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="7412e-127">Error Code</span></span>              | <span data-ttu-id="7412e-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7412e-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7412e-129">\_timeout errore</span><span class="sxs-lookup"><span data-stu-id="7412e-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="7412e-130">Timeout del comando.</span><span class="sxs-lookup"><span data-stu-id="7412e-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="7412e-131">ERRORE \_ req \_ non \_ definit</span><span class="sxs-lookup"><span data-stu-id="7412e-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="7412e-132">Il dispositivo non ha accettato il comando.</span><span class="sxs-lookup"><span data-stu-id="7412e-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="7412e-133">ERRORE \_ non \_ supportato</span><span class="sxs-lookup"><span data-stu-id="7412e-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="7412e-134">Il dispositivo non supporta il comando.</span><span class="sxs-lookup"><span data-stu-id="7412e-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="7412e-135">richiesta di errore \_ \_ interrotta</span><span class="sxs-lookup"><span data-stu-id="7412e-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="7412e-136">Il comando è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="7412e-136">The command was aborted.</span></span> <span data-ttu-id="7412e-137">Possbly il dispositivo è stato rimosso o si è verificata una reimpostazione del bus.</span><span class="sxs-lookup"><span data-stu-id="7412e-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="7412e-138">Questi errori vengono restituiti come codici di errore Win32, non HRESULT, quindi è consigliabile eseguire il test direttamente di questi valori, anziché utilizzare le macro **succeeded** e **failed** .</span><span class="sxs-lookup"><span data-stu-id="7412e-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="7412e-139">Se il metodo restituisce S \_ OK, la risposta dal dispositivo viene copiata nella matrice.</span><span class="sxs-lookup"><span data-stu-id="7412e-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="7412e-140">Il payload della risposta potrebbe essere più grande del comando, quindi è necessario allocare un buffer sufficientemente grande da contenerlo.</span><span class="sxs-lookup"><span data-stu-id="7412e-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="7412e-141">Le dimensioni massime del payload sono pari a 512 byte.</span><span class="sxs-lookup"><span data-stu-id="7412e-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="7412e-142">Si noti che un valore restituito di S \_ OK non sempre significa che il dispositivo ha eseguito correttamente il comando.</span><span class="sxs-lookup"><span data-stu-id="7412e-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="7412e-143">Per determinare lo stato, l'applicazione deve esaminare il payload della risposta.</span><span class="sxs-lookup"><span data-stu-id="7412e-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="7412e-144">Nell'esempio seguente viene illustrato il comando per cercare una ricerca di un numero di traccia assoluto:</span><span class="sxs-lookup"><span data-stu-id="7412e-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="7412e-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7412e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7412e-146">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="7412e-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



