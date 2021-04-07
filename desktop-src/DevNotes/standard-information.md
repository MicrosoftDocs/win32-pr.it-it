---
description: Contiene l'attributo di informazioni standard. Questo attributo è presente in ogni record di file di base e deve essere residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Struttura STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049077"
---
# <a name="standard_information-structure"></a><span data-ttu-id="7d0d4-104">\_Struttura delle informazioni standard</span><span class="sxs-lookup"><span data-stu-id="7d0d4-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="7d0d4-105">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="7d0d4-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="7d0d4-106">Contiene l'attributo di informazioni standard.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-106">Contains the standard information attribute.</span></span> <span data-ttu-id="7d0d4-107">Questo attributo è presente in ogni record di file di base e deve essere residente.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d0d4-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="7d0d4-109">Members</span><span class="sxs-lookup"><span data-stu-id="7d0d4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d0d4-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="7d0d4-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7d0d4-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7d0d4-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="7d0d4-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="7d0d4-113">Identificatore del proprietario del file, dall'indice di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="7d0d4-114">**SecurityId**</span><span class="sxs-lookup"><span data-stu-id="7d0d4-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="7d0d4-115">Identificatore di sicurezza per il file.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d0d4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d0d4-116">Remarks</span></span>

<span data-ttu-id="7d0d4-117">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="7d0d4-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="7d0d4-118">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="7d0d4-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d0d4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d0d4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0d4-120">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="7d0d4-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
