---
description: MFTrace è uno strumento per la generazione di log di traccia per applicazioni Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325218"
---
# <a name="mftrace"></a><span data-ttu-id="6f4b4-103">MFTrace</span><span class="sxs-lookup"><span data-stu-id="6f4b4-103">MFTrace</span></span>

<span data-ttu-id="6f4b4-104">MFTrace è uno strumento per la generazione di log di traccia per applicazioni Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6f4b4-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f4b4-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6f4b4-105">In this section</span></span>

-   [<span data-ttu-id="6f4b4-106">Uso di MFTrace</span><span class="sxs-lookup"><span data-stu-id="6f4b4-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="6f4b4-107">Parole chiave MFTrace</span><span class="sxs-lookup"><span data-stu-id="6f4b4-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="6f4b4-108">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="6f4b4-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="6f4b4-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f4b4-109">Requirements</span></span>



| <span data-ttu-id="6f4b4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4b4-110">Requirement</span></span> | <span data-ttu-id="6f4b4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="6f4b4-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4b4-112">Versione minima dell'SDK</span><span class="sxs-lookup"><span data-stu-id="6f4b4-112">Minimum SDK version</span></span>      | <span data-ttu-id="6f4b4-113">Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="6f4b4-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="6f4b4-114">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="6f4b4-114">Minimum operating system</span></span> | <span data-ttu-id="6f4b4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f4b4-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="6f4b4-116">MFTrace richiede le DLL seguenti, fornite anche nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="6f4b4-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="6f4b4-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="6f4b4-117">detoured.dll</span></span>
-   <span data-ttu-id="6f4b4-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="6f4b4-118">mfdetours.dll</span></span>

<span data-ttu-id="6f4b4-119">L'SDK fornisce le versioni di MFTrace a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6f4b4-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="6f4b4-120">MFTrace non supporta WOW64; per tracciare un processo a 32 bit in esecuzione su Windows a 64 bit, usare la versione a 32 bit di MFTrace.</span><span class="sxs-lookup"><span data-stu-id="6f4b4-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="6f4b4-121">SDK-root nei sistemi a 32 bit: \Programmi\microsoft Kits\10 SDK-root in 64 bit System: \Program Files (x86) \Windows Kits\10 sono disponibili mftrace in <SDK-root> \bin \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="6f4b4-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f4b4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f4b4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f4b4-123">Strumenti di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f4b4-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



