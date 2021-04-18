---
description: Descrive i formati di ora supportati per l'utilizzo nella clausola WHERE di WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formati di WQL-Supported ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310318"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="3c6a6-103">Formati di WQL-Supported ora</span><span class="sxs-lookup"><span data-stu-id="3c6a6-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="3c6a6-104">Oltre al formato DATETIME WMI, i formati di data seguenti sono supportati per l'utilizzo nella clausola WHERE di WQL.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="3c6a6-105">Formato</span><span class="sxs-lookup"><span data-stu-id="3c6a6-105">Format</span></span>                                    | <span data-ttu-id="3c6a6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c6a6-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6a6-107">HH \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="3c6a6-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="3c6a6-108">Ora, come illustrato in un orario a dodici ore e designazione AM o PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="3c6a6-109">4 PM</span><span class="sxs-lookup"><span data-stu-id="3c6a6-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c6a6-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="3c6a6-110">hh:mm</span></span><br/>                          | <span data-ttu-id="3c6a6-111">Ora e minuti delimitati da due punti.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="3c6a6-112">Nessuna designazione AM o PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="3c6a6-113">3:23</span><span class="sxs-lookup"><span data-stu-id="3c6a6-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="3c6a6-114">HH: mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="3c6a6-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="3c6a6-115">Ora e minuti delimitati da due punti, spazio facoltativo e designazione AM o PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="3c6a6-116">3:23 AM</span><span class="sxs-lookup"><span data-stu-id="3c6a6-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="3c6a6-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="3c6a6-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="3c6a6-118">Due punti: ora, minuti e secondi delimitati.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="3c6a6-119">Nessuna indicazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="3c6a6-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="3c6a6-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="3c6a6-121">HH: mm: SS \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="3c6a6-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="3c6a6-122">Ora, minuti e secondi delimitati da due punti, spazio facoltativo e designazione AM/PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="3c6a6-123">3:23: PM</span><span class="sxs-lookup"><span data-stu-id="3c6a6-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="3c6a6-124">HH: mm: SS: UUU</span><span class="sxs-lookup"><span data-stu-id="3c6a6-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="3c6a6-125">Ora, minuti e secondi delimitati da due punti e offset di tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="3c6a6-126">HH: mm: SS: \[ \[ u \] u \] u</span><span class="sxs-lookup"><span data-stu-id="3c6a6-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="3c6a6-127">Due punti: ora, minuti e secondi delimitati; un offset di uno, due o tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="3c6a6-128">HH: mm: SS: UUU \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="3c6a6-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="3c6a6-129">Ora, minuti e secondi delimitati da due punti, offset di tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC e la designazione AM o PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="3c6a6-130">HH: mm: SS: \[ \[ u \] u \] u \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="3c6a6-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="3c6a6-131">Due punti: ora, minuti e secondi delimitati; offset uno, due o tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC; e la designazione AM o PM.</span><span class="sxs-lookup"><span data-stu-id="3c6a6-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3c6a6-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c6a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6a6-133">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="3c6a6-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




