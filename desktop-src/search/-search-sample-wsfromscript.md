---
description: Nell'esempio di codice WSFromScript viene illustrato come eseguire una query su Windows Search da uno script di Microsoft Visual Basic utilizzando Microsoft ActiveX Data Objects (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: WSFromScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342971"
---
# <a name="wsfromscript"></a><span data-ttu-id="c03d5-103">WSFromScript</span><span class="sxs-lookup"><span data-stu-id="c03d5-103">WSFromScript</span></span>

<span data-ttu-id="c03d5-104">Nell'esempio di codice WSFromScript viene illustrato come eseguire una query su Windows Search da uno script di Microsoft Visual Basic utilizzando Microsoft ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="c03d5-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="c03d5-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c03d5-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c03d5-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c03d5-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c03d5-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c03d5-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c03d5-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c03d5-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c03d5-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c03d5-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c03d5-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c03d5-110">Requirements</span></span>

| <span data-ttu-id="c03d5-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c03d5-111">Product</span></span>     | <span data-ttu-id="c03d5-112">Versione prodotto</span><span class="sxs-lookup"><span data-stu-id="c03d5-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c03d5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c03d5-113">Windows</span></span>     | <span data-ttu-id="c03d5-114">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="c03d5-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c03d5-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c03d5-115">Windows SDK</span></span> | <span data-ttu-id="c03d5-116">7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c03d5-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c03d5-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c03d5-117">Downloading the Sample</span></span>

<span data-ttu-id="c03d5-118">Questo esempio è disponibile nel percorso seguente.</span><span class="sxs-lookup"><span data-stu-id="c03d5-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="c03d5-119">Location</span><span class="sxs-lookup"><span data-stu-id="c03d5-119">Location</span></span>      | <span data-ttu-id="c03d5-120">URL percorso</span><span class="sxs-lookup"><span data-stu-id="c03d5-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c03d5-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="c03d5-121">GitHub</span></span>  | [<span data-ttu-id="c03d5-122">Esempio WSFromScript</span><span class="sxs-lookup"><span data-stu-id="c03d5-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="c03d5-123">Per tutte le versioni di Windows, incluso Windows 7, è consigliabile scaricare gli esempi direttamente da GitHub per la versione più aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c03d5-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c03d5-124">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c03d5-124">Building the Sample</span></span>

<span data-ttu-id="c03d5-125">Per compilare l'esempio dalla finestra del prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c03d5-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="c03d5-126">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **QueryEverything** .</span><span class="sxs-lookup"><span data-stu-id="c03d5-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="c03d5-127">Il percorso di installazione predefinito completo di Windows 7 SDK è ad esempio `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="c03d5-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="c03d5-128">Immettere `cscript QueryEverything.vbs`.</span><span class="sxs-lookup"><span data-stu-id="c03d5-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c03d5-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c03d5-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="c03d5-130">Informazioni concettuali</span><span class="sxs-lookup"><span data-stu-id="c03d5-130">Conceptual</span></span>

<span data-ttu-id="c03d5-131">[**Riferimenti per il linguaggio VBScript**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="c03d5-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="c03d5-132">Altri esempi</span><span class="sxs-lookup"><span data-stu-id="c03d5-132">Other Samples</span></span>

[<span data-ttu-id="c03d5-133">Esempi di codice di ricerca</span><span class="sxs-lookup"><span data-stu-id="c03d5-133">Search Code Samples</span></span>](-search-samples-ovw.md)
