---
description: CABINETDLLVERSIONINFO contiene le informazioni sulla versione per Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Struttura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877653"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="553f8-103">Struttura CABINETDLLVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="553f8-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="553f8-104">\[Questa struttura contiene le informazioni necessarie solo quando si usa la funzione **DllGetVersion** , che non è supportata.</span><span class="sxs-lookup"><span data-stu-id="553f8-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="553f8-105">Questa documentazione viene fornita solo a scopo informativo.\]</span><span class="sxs-lookup"><span data-stu-id="553f8-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="553f8-106">**CABINETDLLVERSIONINFO** contiene le informazioni sulla versione per Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="553f8-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="553f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="553f8-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="553f8-108">Members</span><span class="sxs-lookup"><span data-stu-id="553f8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="553f8-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="553f8-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="553f8-110">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="553f8-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="553f8-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="553f8-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="553f8-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="553f8-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="553f8-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="553f8-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="553f8-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="553f8-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="553f8-115">**dwFileVersionMS**</span><span class="sxs-lookup"><span data-stu-id="553f8-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="553f8-116">Contiene i bit più significativi delle informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="553f8-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="553f8-117">BITS 0-15 contengono la versione secondaria e BITS 16-31 contengono la versione principale.</span><span class="sxs-lookup"><span data-stu-id="553f8-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="553f8-118">**dwFileVersionLS**</span><span class="sxs-lookup"><span data-stu-id="553f8-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="553f8-119">Contiene i bit meno significativi delle informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="553f8-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="553f8-120">BITS 0-15 contengono il numero di revisione e BITS 16-31 contengono il numero di Build.</span><span class="sxs-lookup"><span data-stu-id="553f8-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="553f8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="553f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553f8-122">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="553f8-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



