---
title: Inizializzazione del nastro
description: Per creare un handle di un dispositivo nastro, un'applicazione deve utilizzare la funzione CreateFile. Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup inizializzazione nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473678"
---
# <a name="tape-initialization"></a><span data-ttu-id="89217-105">Inizializzazione del nastro</span><span class="sxs-lookup"><span data-stu-id="89217-105">Tape Initialization</span></span>

<span data-ttu-id="89217-106">Per creare un handle di un dispositivo nastro, un'applicazione deve utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="89217-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="89217-107">Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89217-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="89217-108">Prima di scrivere su un nastro, un'applicazione deve essere formattata in base alle esigenze dell'applicazione e alle funzionalità dell'unità nastro utilizzata.</span><span class="sxs-lookup"><span data-stu-id="89217-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="89217-109">La funzione [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) riformatta un nastro, creando un determinato numero di partizioni di una dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="89217-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="89217-110">La funzione [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara un nastro per l'accesso o la rimozione.</span><span class="sxs-lookup"><span data-stu-id="89217-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="89217-111">Questa funzione può caricare, scaricare, bloccare o sbloccare un nastro.</span><span class="sxs-lookup"><span data-stu-id="89217-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="89217-112">Questa funzione può anche eseguire il tensionamento del nastro spostando il nastro alla fine del nastro e tornando all'inizio.</span><span class="sxs-lookup"><span data-stu-id="89217-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="89217-113">Per recuperare e impostare le informazioni su un'unità nastro e nastro, un'applicazione utilizza le funzioni [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="89217-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="89217-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera le informazioni che descrivono un nastro o un'unità nastro.</span><span class="sxs-lookup"><span data-stu-id="89217-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="89217-115">Le informazioni sul nastro includono tipo, densità e dimensione del blocco del nastro; il numero di partizioni sul nastro; quantità di nastri rimanenti; E così via.</span><span class="sxs-lookup"><span data-stu-id="89217-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="89217-116">Le informazioni sulle unità nastro includono le dimensioni del blocco predefinite dell'unità, il numero massimo di partizioni e le funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="89217-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="89217-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) imposta la dimensione del blocco del nastro o imposta i flag di unità nastro che indicano se l'unità supporta la correzione degli errori hardware, la compressione dei dati, il riempimento dei dati o qualsiasi combinazione dei tre.</span><span class="sxs-lookup"><span data-stu-id="89217-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="89217-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica se l'unità nastro è pronta per l'elaborazione dei comandi del nastro.</span><span class="sxs-lookup"><span data-stu-id="89217-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 