---
description: Applicazione WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Applicazione WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751183"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="896c8-103">Applicazione WpdApiSample</span><span class="sxs-lookup"><span data-stu-id="896c8-103">WpdApiSample Application</span></span>

<span data-ttu-id="896c8-104">L'applicazione di esempio WpdApiSample è un'applicazione desktop da riga di comando che consente di enumerare i dispositivi connessi, esplorare i dispositivi, eseguire query sugli oggetti per proprietà e attributi, inviare e recuperare oggetti e così via.</span><span class="sxs-lookup"><span data-stu-id="896c8-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="896c8-105">All'avvio, l'applicazione apre una finestra di comando in cui sono elencate le attività che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="896c8-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="896c8-106">L'applicazione di esempio WpdApiSample include i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="896c8-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="896c8-107">**File**</span><span class="sxs-lookup"><span data-stu-id="896c8-107">**File**</span></span>               | <span data-ttu-id="896c8-108">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="896c8-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="896c8-109">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="896c8-110">Contiene funzioni che enumerano tutti gli oggetti in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896c8-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="896c8-111">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="896c8-112">Contiene funzioni che leggono e scrivono le proprietà degli oggetti ed effettuano richieste Bulk set/get.</span><span class="sxs-lookup"><span data-stu-id="896c8-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="896c8-113">ContentTransfer. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="896c8-114">Contiene funzioni che trasferiscono il contenuto al o dal dispositivo, leggono i requisiti del tipo di oggetto e creano una cartella nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896c8-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="896c8-115">DeviceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="896c8-116">Contiene funzioni per elencare i tipi di oggetto funzionali nel dispositivo, elencare i tipi di contenuto supportati da ogni tipo di oggetto funzionale e visualizzare i profili degli oggetti di rendering.</span><span class="sxs-lookup"><span data-stu-id="896c8-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="896c8-117">DeviceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="896c8-118">Elenca i nomi descrittivi, i produttori e le descrizioni di tutti i dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="896c8-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="896c8-119">DeviceEvents. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="896c8-120">Contiene funzioni che registrano gli eventi del dispositivo e i relativi parametri ogni volta che vengono generati eventi.</span><span class="sxs-lookup"><span data-stu-id="896c8-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="896c8-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-121">Stdafx.cpp</span></span>             | <span data-ttu-id="896c8-122">Include i file standard.</span><span class="sxs-lookup"><span data-stu-id="896c8-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="896c8-123">WpdApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="896c8-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="896c8-124">Ospita la funzione di avvio **\_ tmain** , che chiama la funzione **DoMenu** locale che visualizza un elenco di dispositivi e attività disponibili e chiama la funzione appropriata per la selezione di menu dell'utente.</span><span class="sxs-lookup"><span data-stu-id="896c8-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="896c8-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="896c8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="896c8-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="896c8-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



