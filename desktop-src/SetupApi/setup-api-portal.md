---
description: Installa driver di dispositivo da programmi con uno script di configurazione e file inf. Scrivere un programma di installazione per la configurazione del dispositivo e l'installazione dei driver. Questa API non è più consigliata per l'installazione di applicazioni software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313277"
---
# <a name="setup-api"></a><span data-ttu-id="8c395-105">API di installazione</span><span class="sxs-lookup"><span data-stu-id="8c395-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="8c395-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="8c395-106">Purpose</span></span>

<span data-ttu-id="8c395-107">L'API di installazione di fornisce un set di funzioni che un'applicazione di installazione chiama per eseguire operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="8c395-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8c395-108">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="8c395-108">Where applicable</span></span>

<span data-ttu-id="8c395-109">Queste funzioni di installazione sono disponibili per lo sviluppo di un'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="8c395-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="8c395-110">Non è più possibile usare l'API di installazione per l'installazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8c395-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="8c395-111">Usare invece il [Windows Installer](/windows/desktop/Msi/windows-installer-portal)per lo sviluppo di programmi di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8c395-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="8c395-112">L'API di installazione continua a essere usata per l'installazione dei driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c395-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="8c395-113">L'API di installazione è destinata allo sviluppo di applicazioni di tipo desktop.</span><span class="sxs-lookup"><span data-stu-id="8c395-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8c395-114">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="8c395-114">Developer audience</span></span>

<span data-ttu-id="8c395-115">Uno sviluppatore può usare l'API di installazione se l'applicazione di installazione richiede le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c395-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="8c395-116">Accodamento di file.</span><span class="sxs-lookup"><span data-stu-id="8c395-116">Queuing of files.</span></span>
-   <span data-ttu-id="8c395-117">Installazione dei file.</span><span class="sxs-lookup"><span data-stu-id="8c395-117">Installation of files.</span></span>
-   <span data-ttu-id="8c395-118">Gestione degli errori di installazione e della richiesta di supporto.</span><span class="sxs-lookup"><span data-stu-id="8c395-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="8c395-119">Aggiornamento delle voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8c395-119">Updating registry entries.</span></span>
-   <span data-ttu-id="8c395-120">Registrazione dei file durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8c395-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="8c395-121">Archiviazione dei percorsi di origine usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="8c395-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8c395-122">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="8c395-122">Run-time requirements</span></span>

<span data-ttu-id="8c395-123">Per informazioni sui sistemi operativi necessari per usare una funzione specifica, vedere la sezione requisiti della documentazione relativa alla funzione.</span><span class="sxs-lookup"><span data-stu-id="8c395-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8c395-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8c395-124">In this section</span></span>



| <span data-ttu-id="8c395-125">Argomento</span><span class="sxs-lookup"><span data-stu-id="8c395-125">Topic</span></span>                                 | <span data-ttu-id="8c395-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c395-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c395-127">Overview</span><span class="sxs-lookup"><span data-stu-id="8c395-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="8c395-128">Informazioni generali sull'API di installazione.</span><span class="sxs-lookup"><span data-stu-id="8c395-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="8c395-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8c395-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="8c395-130">Documentazione relativa ai tipi di dati dell'API di installazione, alle strutture, alle funzioni e alle notifiche.</span><span class="sxs-lookup"><span data-stu-id="8c395-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

