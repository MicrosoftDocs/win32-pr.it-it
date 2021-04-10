---
title: Impostazione dell'archivio online iniziale
description: Impostazione dell'archivio online iniziale
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Windows Media Player Online Stores, impostazione degli archivi online iniziali
- negozi online, impostazione degli archivi online iniziali
- digitare 1 negozi online, impostazione degli archivi online iniziali
- digitare 2 archivi online, impostazione degli archivi online iniziali
- Windows Media Player Online Stores, primo negozio online visualizzato
- negozi online, primo negozio online visualizzato
- digitare 1 Store online, primo negozio online visualizzato
- digitare 2 negozi online, primo negozio online visualizzato
- primo negozio online visualizzato
- impostazione degli archivi online iniziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856593"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="bec67-113">Impostazione dell'archivio online iniziale</span><span class="sxs-lookup"><span data-stu-id="bec67-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="bec67-114">Per informazioni dettagliate sulla ridistribuzione del software Windows Media Player con l'applicazione, vedere [ridistribuzione del software windows media player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="bec67-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="bec67-115">Quando un utente installa per la prima volta Windows Media Player, l'applicazione di installazione imposta l'archivio online attivo iniziale su un valore predefinito scelto da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bec67-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="bec67-116">Personal computer Original Equipment Manufacturer (OEM) può scegliere di modificare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="bec67-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="bec67-117">Per specificare e configurare il primo negozio online visualizzato dall'utente durante l'installazione di Windows Media Player, è necessario:</span><span class="sxs-lookup"><span data-stu-id="bec67-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="bec67-118">Creare un documento ServiceInfo da installare sul disco rigido dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bec67-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="bec67-119">Questo documento contiene le informazioni su come configurare l'archivio online attivo iniziale.</span><span class="sxs-lookup"><span data-stu-id="bec67-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="bec67-120">Accoda un set di parametri della riga di comando durante l'esecuzione dell'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="bec67-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="bec67-121">Esistono tre scenari per l'installazione di Windows Media Player e l'impostazione dell'archivio online iniziale.</span><span class="sxs-lookup"><span data-stu-id="bec67-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="bec67-122">Nelle sezioni seguenti vengono forniti ulteriori dettagli su ogni scenario:</span><span class="sxs-lookup"><span data-stu-id="bec67-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="bec67-123">Installazione offline</span><span class="sxs-lookup"><span data-stu-id="bec67-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="bec67-124">Installazione da un CD mentre è in linea</span><span class="sxs-lookup"><span data-stu-id="bec67-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="bec67-125">Installazione dal Web in linea</span><span class="sxs-lookup"><span data-stu-id="bec67-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="bec67-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bec67-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bec67-127">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="bec67-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="bec67-128">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="bec67-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="bec67-129">**Configurare i parametri della riga di comando per i negozi online**</span><span class="sxs-lookup"><span data-stu-id="bec67-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




