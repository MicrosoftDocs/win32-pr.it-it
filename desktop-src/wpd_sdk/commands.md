---
description: Comandi
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandi (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226036"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="c2788-103">Comandi (API WPD)</span><span class="sxs-lookup"><span data-stu-id="c2788-103">Commands (WPD API)</span></span>

<span data-ttu-id="c2788-104">L'applicazione client e il driver comunicano per mezzo di comandi inviati dal client (tramite l'API di Windows Portable Device) al driver (tramite il Framework del driver User-Mode).</span><span class="sxs-lookup"><span data-stu-id="c2788-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="c2788-105">Un comando può includere o meno un parametro e non può restituire un risultato.</span><span class="sxs-lookup"><span data-stu-id="c2788-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="c2788-106">Un client può inviare un comando in modo esplicito, chiamando il metodo [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o **IPortableDeviceService: SendCommand** oppure, in modo implicito, chiamando uno dei metodi delle interfacce client.</span><span class="sxs-lookup"><span data-stu-id="c2788-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="c2788-107">Alcuni comandi possono essere inviati solo in modo esplicito; Questi sono indicati nella documentazione del comando.</span><span class="sxs-lookup"><span data-stu-id="c2788-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="c2788-108">Le pagine di riferimento del comando descrivono lo scopo di un comando, nonché i parametri che prevede di ricevere e i parametri che dovrebbero restituire.</span><span class="sxs-lookup"><span data-stu-id="c2788-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="c2788-109">Un comando è identificato da una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="c2788-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="c2788-110">Questa operazione è costituita da due parti: una parte GUID (membro *fmtid* ) e una parte DWORD (il membro *PID* ).</span><span class="sxs-lookup"><span data-stu-id="c2788-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="c2788-111">La parte GUID viene utilizzata per indicare la categoria a cui appartiene il comando (i comandi correlati appartengono alla stessa categoria e pertanto avranno lo stesso *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="c2788-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="c2788-112">La parte DWORD indica l'ID di comando e viene usata per distinguere i singoli comandi all'interno di una categoria di comandi (i valori *PID* per i comandi nella stessa categoria saranno diversi).</span><span class="sxs-lookup"><span data-stu-id="c2788-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="c2788-113">Nella tabella seguente sono elencate le categorie di comandi definiti da dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="c2788-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="c2788-114">I produttori di dispositivi possono definire i propri comandi creando proprie categorie di comando e ID di comando.</span><span class="sxs-lookup"><span data-stu-id="c2788-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="c2788-115">Tuttavia, un produttore non deve aggiungere comandi alle categorie elencate di seguito, perché sono riservate da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2788-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="c2788-116">**Categorie di comandi**</span><span class="sxs-lookup"><span data-stu-id="c2788-116">**Command Categories**</span></span>



| <span data-ttu-id="c2788-117">Categoria</span><span class="sxs-lookup"><span data-stu-id="c2788-117">Command category</span></span>                         | <span data-ttu-id="c2788-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2788-119">**\_categoria WPD \_ comune**</span><span class="sxs-lookup"><span data-stu-id="c2788-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="c2788-120">Comandi comuni a tutti gli oggetti e i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c2788-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="c2788-121">**\_hint per \_ dispositivi di categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="c2788-122">Comandi usati per recuperare informazioni facoltative sul dispositivo che possono essere usate per migliorare l'esperienza dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="c2788-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="c2788-123">**\_SMS della categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="c2788-124">Comandi usati per i dispositivi che supportano la funzionalità SMS (Short Message Service), che in genere è esposta nei telefoni cellulari.</span><span class="sxs-lookup"><span data-stu-id="c2788-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="c2788-125">**\_acquisizione di \_ \_ Immagini ancora della categoria \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="c2788-126">Comandi usati per i dispositivi che supportano l'acquisizione di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="c2788-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="c2788-127">**\_archiviazione categoria \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="c2788-128">Comandi utilizzati per gli oggetti funzionali di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c2788-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="c2788-129">I comandi specifici definiti per ognuno di questi tipi sono forniti nelle tabelle seguenti, organizzati per tipo di comando.</span><span class="sxs-lookup"><span data-stu-id="c2788-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="c2788-130">**\_ \_ Categoria comune categoria WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="c2788-131">Comando</span><span class="sxs-lookup"><span data-stu-id="c2788-131">Command</span></span>                                                                                | <span data-ttu-id="c2788-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="c2788-133">**\_dispositivo di \_ \_ reimpostazione comune comando \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="c2788-134">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2788-134">Resets the device.</span></span> |



 

<span data-ttu-id="c2788-135">**Categoria \_ di \_ hint del dispositivo categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="c2788-136">Comando</span><span class="sxs-lookup"><span data-stu-id="c2788-136">Command</span></span>                                                                                                              | <span data-ttu-id="c2788-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="c2788-138">**\_suggerimenti del \_ dispositivo comando WPD ottenere il \_ \_ \_ percorso del contenuto \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="c2788-139">Recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="c2788-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="c2788-140">**\_ \_ Categoria archiviazione categoria WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="c2788-141">Comando</span><span class="sxs-lookup"><span data-stu-id="c2788-141">Command</span></span>                                                                     | <span data-ttu-id="c2788-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="c2788-143">**\_espulsione \_ archiviazione comando WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="c2788-144">Espelle un supporto di archiviazione che può essere espulso in remoto dal driver.</span><span class="sxs-lookup"><span data-stu-id="c2788-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="c2788-145">**\_formato di \_ archiviazione \_ comando WPD**</span><span class="sxs-lookup"><span data-stu-id="c2788-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="c2788-146">Formatta un oggetto funzionale di archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2788-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="c2788-147">**Categoria \_ SMS categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="c2788-148">Comando</span><span class="sxs-lookup"><span data-stu-id="c2788-148">Command</span></span>                                                         | <span data-ttu-id="c2788-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="c2788-150">**\_comando WPD \_ SMS \_ Send**</span><span class="sxs-lookup"><span data-stu-id="c2788-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="c2788-151">Avvia l'invio di un messaggio SMS da un oggetto funzionale SMS.</span><span class="sxs-lookup"><span data-stu-id="c2788-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="c2788-152">**Categoria \_ WPD \_ still \_ Image \_ Capture**</span><span class="sxs-lookup"><span data-stu-id="c2788-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="c2788-153">Comando</span><span class="sxs-lookup"><span data-stu-id="c2788-153">Command</span></span>                                                                                                   | <span data-ttu-id="c2788-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2788-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="c2788-155">**il \_ comando WPD ha \_ ancora \_ avviato l'acquisizione dell'immagine \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c2788-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="c2788-156">Avvia un'acquisizione di immagini ancora da un oggetto funzionale dell'immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="c2788-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c2788-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2788-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2788-158">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="c2788-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



