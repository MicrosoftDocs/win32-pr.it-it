---
description: Glossario dei termini Network Monitor che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311639"
---
# <a name="c-network-monitor"></a><span data-ttu-id="4066b-103">C (Network Monitor)</span><span class="sxs-lookup"><span data-stu-id="4066b-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="4066b-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**catturare**</span><span class="sxs-lookup"><span data-stu-id="4066b-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-105">Dati relativi al traffico di rete raccolti in frame.</span><span class="sxs-lookup"><span data-stu-id="4066b-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="4066b-106">Un provider di pacchetti di rete (NPP) esegue un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="4066b-107">Vedere anche [*acquisizione ritardata*](d.md)e *acquisizione in tempo reale*</span><span class="sxs-lookup"><span data-stu-id="4066b-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="4066b-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**Acquisisci file**</span><span class="sxs-lookup"><span data-stu-id="4066b-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-109">File creato da Network Monitor per archiviare i dati acquisiti.</span><span class="sxs-lookup"><span data-stu-id="4066b-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="4066b-110">L'estensione del nome file. Cap identifica un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="4066b-111">Network Monitor genera in modo casuale un nome file di acquisizione, ma è possibile modificare il nome del file quando si salva il file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="4066b-112">Network Monitor crea un file di acquisizione ogni volta che il processo di acquisizione viene avviato e quindi mantiene aperto il file durante il processo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="4066b-113">Non è possibile accedere al contenuto di un file di acquisizione finché il processo di acquisizione non viene arrestato e il file di acquisizione viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="4066b-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="4066b-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro di acquisizione**</span><span class="sxs-lookup"><span data-stu-id="4066b-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-115">Set di funzioni Network Monitor utilizzate per limitare i frame in ingresso utilizzati da un'applicazione di provider di pacchetti di rete (NPP).</span><span class="sxs-lookup"><span data-stu-id="4066b-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="4066b-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**trigger di acquisizione**</span><span class="sxs-lookup"><span data-stu-id="4066b-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-117">Evento trigger impostato per arrestare il processo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="4066b-118">L'evento di acquisizione del trigger può essere un file di acquisizione temporaneo indirizzato a un livello specifico o a un modello di dati che si verifica in un frame acquisito.</span><span class="sxs-lookup"><span data-stu-id="4066b-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="4066b-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**dati acquisiti**</span><span class="sxs-lookup"><span data-stu-id="4066b-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-120">Frame che dispongono di un set definito di criteri.</span><span class="sxs-lookup"><span data-stu-id="4066b-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="4066b-121">I frame di dati sono contenuti in un file di acquisizione temporaneo.</span><span class="sxs-lookup"><span data-stu-id="4066b-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="4066b-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Statistiche sulle conversazioni**</span><span class="sxs-lookup"><span data-stu-id="4066b-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="4066b-123">Statistiche del traffico di rete salvato durante un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4066b-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="4066b-124">Queste statistiche includono le informazioni sulle stazioni e sulle sessioni che iniziano quando il processo di acquisizione viene avviato e terminano quando l'acquisizione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="4066b-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="4066b-125">Se si sospende il processo di acquisizione, Network Monitor continua ad aggiungere statistiche quando si riprende il processo.</span><span class="sxs-lookup"><span data-stu-id="4066b-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="4066b-126">Per recuperare le statistiche di conversazione, chiamare il metodo **GetConversationStatistics** per l'interfaccia in uso.</span><span class="sxs-lookup"><span data-stu-id="4066b-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



