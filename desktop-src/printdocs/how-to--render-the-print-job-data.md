---
description: In questo argomento viene descritto come eseguire il rendering dei dati del programma da stampare.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Procedura: eseguire il rendering dei dati del processo di stampa'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885177"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="ef236-103">Procedura: eseguire il rendering dei dati del processo di stampa</span><span class="sxs-lookup"><span data-stu-id="ef236-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="ef236-104">In questo argomento viene descritto come eseguire il rendering dei dati del programma da stampare.</span><span class="sxs-lookup"><span data-stu-id="ef236-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="ef236-105">In questo argomento non viene illustrato in dettaglio come eseguire il rendering di immagini grafiche o di testo specifiche.</span><span class="sxs-lookup"><span data-stu-id="ef236-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="ef236-106">Viene invece descritto come gestire i dati di programma ed eseguirne il rendering come documento XPS, che viene inviato a una stampante tramite l' [API di stampa XPS](xps-printing.md).</span><span class="sxs-lookup"><span data-stu-id="ef236-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="ef236-107">Panoramica</span><span class="sxs-lookup"><span data-stu-id="ef236-107">Overview</span></span>

<span data-ttu-id="ef236-108">Il rendering dei dati dei processi di stampa per la stampa comporta l'esecuzione di dati specifici del programma, ad esempio testo, immagini e formattazione, e la relativa conversione in un formato compatibile con la stampante di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef236-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="ef236-109">Il programma che invia i dati alla stampante deve inviarlo nel formato richiesto dal driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="ef236-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="ef236-110">Utilizzare l' [API di stampa XPS](xps-printing.md) per inviare i dati alla stampante ed è necessario che i dati vengano formattati come documento XPS.</span><span class="sxs-lookup"><span data-stu-id="ef236-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="ef236-111">Per produrre il contenuto del documento XPS necessario per l'API di stampa XPS, il programma di esempio utilizza l' [API del documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef236-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="ef236-112">Se il contenuto del programma è in un formato non compatibile con una stampante, sarà necessario eseguirne il rendering prima di inviarlo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="ef236-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="ef236-113">Se il programma utilizza l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) per gestire il contenuto del programma, il contenuto del programma sarà in un formato che può essere inviato direttamente all' [API di stampa XPS](xps-printing.md) e non sarà necessario alcun rendering aggiuntivo prima di inviarlo alla stampante.</span><span class="sxs-lookup"><span data-stu-id="ef236-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef236-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef236-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ef236-115">[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef236-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef236-116">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="ef236-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
