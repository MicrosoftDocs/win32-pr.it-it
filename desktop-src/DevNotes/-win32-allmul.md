---
title: Routine di _allmul
description: Moltiplica due Integer LONGLONG o ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104046221"
---
# <a name="_allmul-routine"></a><span data-ttu-id="c0776-103">\_Routine allmul</span><span class="sxs-lookup"><span data-stu-id="c0776-103">\_allmul Routine</span></span>

<span data-ttu-id="c0776-104">Moltiplica due integer **LONGLONG** o **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="c0776-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="c0776-105">Ad esempio, per moltiplicare due valori Int64, il compilatore potrebbe generare una chiamata alla routine **\_ allmul** .</span><span class="sxs-lookup"><span data-stu-id="c0776-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0776-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0776-106">Remarks</span></span>

<span data-ttu-id="c0776-107">La routine **\_ allmul** è una routine di supporto per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="c0776-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="c0776-108">Il fatto che il compilatore usi **\_ allmul** dipenda completamente dal set di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="c0776-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="c0776-109">Questa routine viene utilizzata solo su piattaforme x86.</span><span class="sxs-lookup"><span data-stu-id="c0776-109">This routine is used only on x86 platforms.</span></span>
