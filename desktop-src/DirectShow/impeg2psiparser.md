---
description: L'implementazione di questa interfaccia viene fornita come codice di esempio con DirectShow SDK.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interfaccia IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303814"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="34649-103">Interfaccia IMpeg2PsiParser</span><span class="sxs-lookup"><span data-stu-id="34649-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="34649-104">L'implementazione di questa interfaccia viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="34649-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="34649-105">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="34649-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="34649-106">L' `IMpeg2PsiParser` interfaccia recupera le informazioni specifiche del programma (PSI) dal filtro del parser PSI, fornito in DIRECTSHOW SDK come filtro di esempio.</span><span class="sxs-lookup"><span data-stu-id="34649-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="34649-107">Un'applicazione può utilizzare questo filtro per eseguire il mapping degli ID programma (PID) nel filtro MPEG-2 Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="34649-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="34649-108">Membri</span><span class="sxs-lookup"><span data-stu-id="34649-108">Members</span></span>

<span data-ttu-id="34649-109">L'interfaccia **IMpeg2PsiParser** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="34649-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34649-110">**IMpeg2PsiParser** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="34649-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="34649-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="34649-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="34649-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="34649-112">Methods</span></span>

<span data-ttu-id="34649-113">L'interfaccia **IMpeg2PsiParser** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="34649-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="34649-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="34649-114">Method</span></span>                                                                             | <span data-ttu-id="34649-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34649-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="34649-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34649-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="34649-117">Trova il PID della tabella di mappa dei programmi (PMT) per un programma, in base al numero di programma.</span><span class="sxs-lookup"><span data-stu-id="34649-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="34649-118">**GetCountOfElementaryStreams**</span><span class="sxs-lookup"><span data-stu-id="34649-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="34649-119">Recupera il numero di flussi elementari in un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="34649-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="34649-120">**GetCountOfPrograms**</span><span class="sxs-lookup"><span data-stu-id="34649-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="34649-121">Recupera il numero di programmi nel flusso di trasporto.</span><span class="sxs-lookup"><span data-stu-id="34649-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="34649-122">**GetPatVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="34649-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="34649-123">Recupera il \_ campo del numero di versione dalla tabella di associazione dei programmi (Pat).</span><span class="sxs-lookup"><span data-stu-id="34649-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="34649-124">**GetPmtVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="34649-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="34649-125">Recupera il \_ campo del numero di versione da un PMT specificato.</span><span class="sxs-lookup"><span data-stu-id="34649-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="34649-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34649-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="34649-127">Recupera l'assegnazione PID per un flusso elementare specificato in un programma.</span><span class="sxs-lookup"><span data-stu-id="34649-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="34649-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34649-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="34649-129">Recupera l'assegnazione PID per un valore PMT specificato.</span><span class="sxs-lookup"><span data-stu-id="34649-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="34649-130">**GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="34649-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="34649-131">Recupera il numero di programma per un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="34649-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="34649-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34649-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="34649-133">Recupera il tipo di flusso per un flusso elementare specificato in un programma.</span><span class="sxs-lookup"><span data-stu-id="34649-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="34649-134">**GetTransportStreamId**</span><span class="sxs-lookup"><span data-stu-id="34649-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="34649-135">Recupera il \_ \_ campo ID del flusso di trasporto da Pat.</span><span class="sxs-lookup"><span data-stu-id="34649-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="34649-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34649-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34649-137">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="34649-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
