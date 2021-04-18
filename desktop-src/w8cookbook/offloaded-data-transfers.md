---
title: Trasferimenti dati scaricati
description: Trasferimenti dati scaricati
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- copia offload
- Offload
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300569"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="5d498-106">Trasferimenti dati scaricati</span><span class="sxs-lookup"><span data-stu-id="5d498-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="5d498-107">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="5d498-107">Platforms</span></span>

<span data-ttu-id="5d498-108">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d498-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="5d498-109">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d498-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="5d498-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d498-110">Description</span></span>

<span data-ttu-id="5d498-111">Per promuovere lo spostamento dei dati di archiviazione, Microsoft ha sviluppato una nuova tecnologia di trasferimento dei dati (ODX).</span><span class="sxs-lookup"><span data-stu-id="5d498-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="5d498-112">Invece di usare le operazioni di scrittura con memorizzazione nel buffer e di lettura memorizzate nel buffer, Windows ODX avvia l'operazione di copia con un offload Read e recupera un token che rappresenta i dati dal dispositivo di archiviazione, quindi usa un comando offload Write con il token per richiedere lo spostamento dei dati dal disco di origine al disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d498-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="5d498-113">Il gestore delle copie dei dispositivi di archiviazione esegue lo spostamento dei dati in base al token.</span><span class="sxs-lookup"><span data-stu-id="5d498-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="5d498-114">In Windows 8, il responsabile IT e l'amministratore di archiviazione sono in grado di utilizzare la funzionalità Windows ODX per interagire con il dispositivo di archiviazione per spostare file o dati di grandi dimensioni tramite la rete di archiviazione ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="5d498-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="5d498-115">Windows ODX ridurrà significativamente il traffico di rete client-server e l'utilizzo della CPU durante i trasferimenti di dati di grandi dimensioni, perché tutto lo spostamento dei dati si trova nella rete di archiviazione back-end.</span><span class="sxs-lookup"><span data-stu-id="5d498-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="5d498-116">ODX può essere usato per la distribuzione di macchine virtuali, la migrazione massiccia dei dati e il supporto dei dispositivi di archiviazione a più livelli e può ridurre i costi di distribuzione dell'hardware fisico tramite le funzionalità di archiviazione ODX e thin provisioning.</span><span class="sxs-lookup"><span data-stu-id="5d498-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="5d498-117">Questa funzionalità funzionerà solo sui dispositivi di archiviazione con implementazione della specifica SPC4 e SBC3.</span><span class="sxs-lookup"><span data-stu-id="5d498-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="5d498-118">Dettagli funzionali</span><span class="sxs-lookup"><span data-stu-id="5d498-118">Functional details</span></span>

-   <span data-ttu-id="5d498-119">La funzionalità ODX di Windows è incorporata nel motore di copia del sistema operativo Windows; durante l'enumerazione dell'archiviazione, Windows eseguirà una query sulla funzionalità ODX del dispositivo di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5d498-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="5d498-120">La copia del dispositivo di archiviazione di origine e della copia di destinazione deve essere gestita nello stesso gestore di copia per il supporto dell'offload di copia</span><span class="sxs-lookup"><span data-stu-id="5d498-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="5d498-121">Se un'operazione di offload di copia non riesce, il gestore delle copie del dispositivo di archiviazione deve restituire i dati di rilevamento appropriati appropriati per la gestione degli errori delle app</span><span class="sxs-lookup"><span data-stu-id="5d498-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="5d498-122">Il motore di copia di Windows eseguirà il fallback all'operazione di copia tradizionale se l'operazione di copia dell'offload non riesce</span><span class="sxs-lookup"><span data-stu-id="5d498-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="5d498-123">Uso di ODX</span><span class="sxs-lookup"><span data-stu-id="5d498-123">Using ODX</span></span>

-   <span data-ttu-id="5d498-124">L'app per il trasferimento dei dati deve garantire che sia il lun di origine della copia sia il LUN di destinazione della copia siano ODX, prima di chiamare le routine dell'API ODX</span><span class="sxs-lookup"><span data-stu-id="5d498-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="5d498-125">In Esplora risorse gli utenti possono usare "trascina" o "copia e incolla" per eseguire l'offload della copia</span><span class="sxs-lookup"><span data-stu-id="5d498-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="5d498-126">Quando il lun di origine e il LUN di destinazione sono montati con la file system, l'app deve chiamare solo FSCTL \_ offload \_ Read e FSCTL \_ offload \_ Write per eseguire il trasferimento dei dati dal LUN di origine al LUN di destinazione</span><span class="sxs-lookup"><span data-stu-id="5d498-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="5d498-127">Se un'operazione di offload di copia non riesce, il gestore delle copie del dispositivo di archiviazione deve restituire i dati di rilevamento aggiuntivi appropriati per la gestione degli errori delle app</span><span class="sxs-lookup"><span data-stu-id="5d498-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="5d498-128">Quando il lun di origine o il LUN di destinazione non è montato con il file system e bloccato, l'app deve chiamare l' \_ archiviazione IOCTL \_ gestire \_ \_ \_ gli attributi del set di dati con DeviceDsmAction \_ OffloadRead o DeviceDsmAction \_ OffloadWrite azione per eseguire l'offload della copia</span><span class="sxs-lookup"><span data-stu-id="5d498-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="5d498-129">Le app per la gestione dell'archiviazione possono usare l' \_ \_ API pass-through SCSI per eseguire trasferimenti di dati con offload quando i LUN di origine e di destinazione non sono montati con alcun file System e bloccato</span><span class="sxs-lookup"><span data-stu-id="5d498-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="5d498-130">Test</span><span class="sxs-lookup"><span data-stu-id="5d498-130">Tests</span></span>

-   <span data-ttu-id="5d498-131">Per garantire un'esperienza utente affidabile, verificare la certificazione Windows ODX dell'array di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5d498-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="5d498-132">Per supportare la funzionalità ODX, il dispositivo di archiviazione deve essere conforme ai requisiti di certificazione per i trasferimenti di dati con offload di Windows (usati per essere logo)</span><span class="sxs-lookup"><span data-stu-id="5d498-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="5d498-133">Utilizzare il kit di certificazione hardware trasferimenti dati scaricati da Windows per verificare il supporto della funzionalità ODX dei dispositivi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5d498-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="5d498-134">Risorse</span><span class="sxs-lookup"><span data-stu-id="5d498-134">Resources</span></span>

-   <span data-ttu-id="5d498-135">Specifiche T10 XCOPY Lite (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="5d498-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="5d498-136">Servizi dashboard hardware</span><span class="sxs-lookup"><span data-stu-id="5d498-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="5d498-137">\_Struttura pass- \_ through SCSI</span><span class="sxs-lookup"><span data-stu-id="5d498-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 