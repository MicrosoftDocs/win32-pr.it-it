---
title: Tag MRK
description: Tag MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710510"
---
# <a name="mrk-tag"></a><span data-ttu-id="30441-103">Tag MRK</span><span class="sxs-lookup"><span data-stu-id="30441-103">Mrk Tag</span></span>

<span data-ttu-id="30441-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30441-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="30441-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="30441-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="30441-106">Definisce un segnalibro nel testo parlato.</span><span class="sxs-lookup"><span data-stu-id="30441-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="30441-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="30441-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="30441-108">**\\MRK =***numero***\\**</span><span class="sxs-lookup"><span data-stu-id="30441-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="30441-109">Parte</span><span class="sxs-lookup"><span data-stu-id="30441-109">Part</span></span>     | <span data-ttu-id="30441-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30441-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="30441-111">*number*</span><span class="sxs-lookup"><span data-stu-id="30441-111">*number*</span></span> | <span data-ttu-id="30441-112">Valore long integer che identifica il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="30441-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="30441-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="30441-113">Remarks</span></span>

<span data-ttu-id="30441-114">Quando il server elabora un segnalibro, genera un evento di segnalibro.</span><span class="sxs-lookup"><span data-stu-id="30441-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="30441-115">È necessario specificare un numero maggiore di zero (0) e non uguale a 2147483647 o 2147483646.</span><span class="sxs-lookup"><span data-stu-id="30441-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




