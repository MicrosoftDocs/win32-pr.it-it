---
description: Nella tabella seguente sono elencate le
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Strumenti dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967500"
---
# <a name="performance-counters-tools"></a><span data-ttu-id="563d8-103">Strumenti dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="563d8-103">Performance Counters Tools</span></span>

## <a name="data-collection-tools"></a><span data-ttu-id="563d8-104">Strumenti di raccolta dati</span><span class="sxs-lookup"><span data-stu-id="563d8-104">Data collection tools</span></span>

<span data-ttu-id="563d8-105">Gli strumenti seguenti sono utili quando si utilizzano o si modificano i dati dei contatori delle prestazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="563d8-105">The following tools are useful when consuming or manipulating Windows Performance Counter data.</span></span>

|<span data-ttu-id="563d8-106">Strumento</span><span class="sxs-lookup"><span data-stu-id="563d8-106">Tool</span></span>|<span data-ttu-id="563d8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563d8-107">Description</span></span>
|----|-----------
| [<span data-ttu-id="563d8-108">PerfMon</span><span class="sxs-lookup"><span data-stu-id="563d8-108">PerfMon</span></span>](/windows-server/administration/windows-commands/perfmon) | <span data-ttu-id="563d8-109">Strumento GUI per la raccolta e la visualizzazione dei dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="563d8-109">GUI tool for collecting and viewing Performance Counter data.</span></span> <span data-ttu-id="563d8-110">`perfmon.exe` Avvia MMC con lo snap-in Performance Monitor, che consente di accedere a performance monitor, insiemi agenti di raccolta dati e strumenti report.</span><span class="sxs-lookup"><span data-stu-id="563d8-110">`perfmon.exe` launches MMC with the Performance Monitor snap-in, which provides access to the Performance Monitor, Data Collector Sets, and Reports tools.</span></span>
| [<span data-ttu-id="563d8-111">TypePerf</span><span class="sxs-lookup"><span data-stu-id="563d8-111">TypePerf</span></span>](/windows-server/administration/windows-commands/typeperf) |<span data-ttu-id="563d8-112">Strumento da riga di comando per la raccolta e la stampa dei dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="563d8-112">Command-line tool for collecting and printing Performance Counter data.</span></span> <span data-ttu-id="563d8-113">Può essere usato per elencare i CounterSet disponibili, elencare i contatori disponibili, stampare i dati del contatore nella console o raccogliere i dati del contatore in un file di log (CSV, TDF, grosso).</span><span class="sxs-lookup"><span data-stu-id="563d8-113">Can be used to list available countersets, list available counters, print counter data to the console, or collect counter data to a log file (CSV, TDF, BLG).</span></span>
| [<span data-ttu-id="563d8-114">Relog</span><span class="sxs-lookup"><span data-stu-id="563d8-114">Relog</span></span>](/windows-server/administration/windows-commands/relog) |<span data-ttu-id="563d8-115">Strumento da riga di comando per la trasformazione e l'Unione di file di log (CSV, TDF, un grosso) acquisiti tramite `typeperf.exe` o tramite le `PDH.dll` API.</span><span class="sxs-lookup"><span data-stu-id="563d8-115">Command-line tool for transforming and merging log files (CSV, TDF, BLG) captured via `typeperf.exe` or via the `PDH.dll` APIs.</span></span>
| [<span data-ttu-id="563d8-116">LogMan</span><span class="sxs-lookup"><span data-stu-id="563d8-116">LogMan</span></span>](/windows-server/administration/windows-commands/logman) |<span data-ttu-id="563d8-117">Strumento da riga di comando per il controllo degli insiemi agenti di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="563d8-117">Command-line tool for controlling Data Collector Sets.</span></span>

## <a name="data-provider-tools"></a><span data-ttu-id="563d8-118">Strumenti del provider di dati</span><span class="sxs-lookup"><span data-stu-id="563d8-118">Data provider tools</span></span>

<span data-ttu-id="563d8-119">Gli strumenti seguenti sono utili quando si pubblicano i dati dei contatori delle prestazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="563d8-119">The following tools are useful when publishing Windows Performance Counter data.</span></span>

|<span data-ttu-id="563d8-120">Strumento</span><span class="sxs-lookup"><span data-stu-id="563d8-120">Tool</span></span>|<span data-ttu-id="563d8-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563d8-121">Description</span></span>
|----|-----------
| [<span data-ttu-id="563d8-122">CtrPP</span><span class="sxs-lookup"><span data-stu-id="563d8-122">CtrPP</span></span>](ctrpp.md) | <span data-ttu-id="563d8-123">Strumento di compilazione da riga di comando dalla Windows SDK che convalida e compila il manifesto del provider v2 dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="563d8-123">Command-line build tool from the Windows SDK that validates and compiles your Performance Counters V2 provider manifest.</span></span> <span data-ttu-id="563d8-124">Questo strumento genera le `.h` intestazioni e gli `.rc` script di risorsa necessari per compilare un provider v2.</span><span class="sxs-lookup"><span data-stu-id="563d8-124">This tool generates the `.h` headers and `.rc` resource scripts needed to build a V2 provider.</span></span>
| [<span data-ttu-id="563d8-125">LodCtr</span><span class="sxs-lookup"><span data-stu-id="563d8-125">LodCtr</span></span>](/windows-server/administration/windows-commands/lodctr) | <span data-ttu-id="563d8-126">Strumento da riga di comando utilizzato per installare il provider in un sistema.</span><span class="sxs-lookup"><span data-stu-id="563d8-126">Command-line tool used to install your provider onto a system.</span></span>
| [<span data-ttu-id="563d8-127">UnlodCtr</span><span class="sxs-lookup"><span data-stu-id="563d8-127">UnlodCtr</span></span>](/windows-server/administration/windows-commands/unlodctr_1) | <span data-ttu-id="563d8-128">Strumento da riga di comando utilizzato per disinstallare il provider da un sistema.</span><span class="sxs-lookup"><span data-stu-id="563d8-128">Command-line tool used to uninstall your provider from a system.</span></span>
