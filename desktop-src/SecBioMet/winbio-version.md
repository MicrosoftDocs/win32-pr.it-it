---
title: Struttura WINBIO_VERSION ( \_ tipi WINBIO. h)
description: Contiene il numero di versione del software di un componente del provider di servizi biometrico.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- Struttura di WINBIO_VERSION Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_VERSION
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479126"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="15864-105">Struttura della versione di WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="15864-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="15864-106">La struttura della **\_ versione WINBIO** contiene il numero di versione del software di un componente del provider di servizi biometrico.</span><span class="sxs-lookup"><span data-stu-id="15864-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="15864-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15864-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="15864-108">Members</span><span class="sxs-lookup"><span data-stu-id="15864-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="15864-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="15864-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="15864-110">**Valore DWORD** che contiene il numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="15864-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="15864-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="15864-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="15864-112">**Valore DWORD** che contiene il numero di versione secondario.</span><span class="sxs-lookup"><span data-stu-id="15864-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15864-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15864-113">Requirements</span></span>



| <span data-ttu-id="15864-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15864-114">Requirement</span></span> | <span data-ttu-id="15864-115">Valore</span><span class="sxs-lookup"><span data-stu-id="15864-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15864-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15864-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15864-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="15864-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="15864-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15864-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15864-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="15864-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="15864-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15864-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15864-121"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15864-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15864-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15864-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15864-123">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="15864-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="15864-124">**\_schema BSP \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="15864-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="15864-125">**\_schema unità \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="15864-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





