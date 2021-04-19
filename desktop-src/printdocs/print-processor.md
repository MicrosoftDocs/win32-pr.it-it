---
description: Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare il momento appropriato per la stampa di un processo.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processore di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311812"
---
# <a name="print-processor"></a><span data-ttu-id="cf775-103">Processore di stampa</span><span class="sxs-lookup"><span data-stu-id="cf775-103">Print Processor</span></span>

<span data-ttu-id="cf775-104">Lo spooler di stampa monitora i processi di stampa correnti e la stampante di destinazione per determinare il momento appropriato per la stampa di un processo.</span><span class="sxs-lookup"><span data-stu-id="cf775-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="cf775-105">Quando lo spooler stabilisce che è necessario stampare un processo, viene chiamato il processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf775-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="cf775-106">Il processore di stampa è un plug-in che elabora i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf775-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="cf775-107">Usare le funzioni seguenti per lavorare con i processori di stampa.</span><span class="sxs-lookup"><span data-stu-id="cf775-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="cf775-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="cf775-108">Function</span></span>                                                           | <span data-ttu-id="cf775-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf775-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="cf775-110">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="cf775-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="cf775-111">Installa un processore di stampa in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="cf775-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="cf775-112">**DeletePrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="cf775-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="cf775-113">Rimuove un processore di stampanti da un server specificato.</span><span class="sxs-lookup"><span data-stu-id="cf775-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="cf775-114">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="cf775-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="cf775-115">Enumera i tipi di dati supportati da un processore di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="cf775-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="cf775-116">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="cf775-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="cf775-117">Enumera i processori di stampa installati in un server specificato.</span><span class="sxs-lookup"><span data-stu-id="cf775-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="cf775-118">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="cf775-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="cf775-119">Recupera il percorso per il processore di stampa nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="cf775-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



