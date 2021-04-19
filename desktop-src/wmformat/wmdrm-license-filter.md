---
title: Struttura WMDRM_LICENSE_FILTER (wmdrmsdk. h)
description: La \_ struttura del filtro delle licenze WMDRM definisce i \_ parametri di filtro da usare durante la creazione di un'enumerazione delle licenze.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- Formato di Windows Media per la struttura WMDRM_LICENSE_FILTER
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326599"
---
# <a name="wmdrm_license_filter-structure"></a><span data-ttu-id="748a3-105">Struttura del filtro delle \_ licenze WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="748a3-105">WMDRM\_LICENSE\_FILTER structure</span></span>

<span data-ttu-id="748a3-106">La struttura del **\_ \_ filtro delle licenze WMDRM** definisce i parametri di filtro da usare durante la creazione di un'enumerazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="748a3-106">The **WMDRM\_LICENSE\_FILTER** structure defines filtering parameters for use when creating a license enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="748a3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="748a3-107">Syntax</span></span>


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a><span data-ttu-id="748a3-108">Members</span><span class="sxs-lookup"><span data-stu-id="748a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="748a3-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="748a3-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="748a3-110">Specifica un numero di versione minimo per le licenze restituite.</span><span class="sxs-lookup"><span data-stu-id="748a3-110">Specifies a minimum version number for the returned licenses.</span></span>

</dd> <dt>

<span data-ttu-id="748a3-111">**bstrKID**</span><span class="sxs-lookup"><span data-stu-id="748a3-111">**bstrKID**</span></span>
</dt> <dd>

<span data-ttu-id="748a3-112">Specifica un ID chiave per il filtro delle licenze.</span><span class="sxs-lookup"><span data-stu-id="748a3-112">Specifies a key ID to filter licenses for.</span></span> <span data-ttu-id="748a3-113">Nell'enumerazione verranno incluse solo le licenze con l'ID chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="748a3-113">Only licenses with the specified key ID will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="748a3-114">**bstrRights**</span><span class="sxs-lookup"><span data-stu-id="748a3-114">**bstrRights**</span></span>
</dt> <dd>

<span data-ttu-id="748a3-115">Specifica un set di diritti per filtrare le licenze per.</span><span class="sxs-lookup"><span data-stu-id="748a3-115">Specifies a set of rights to filter licenses for.</span></span> <span data-ttu-id="748a3-116">Nell'enumerazione verranno incluse solo le licenze che forniscono tutti i diritti specificati.</span><span class="sxs-lookup"><span data-stu-id="748a3-116">Only licenses that provide all of the specified rights will be included in the enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="748a3-117">**bstrAllowedSourceIDs**</span><span class="sxs-lookup"><span data-stu-id="748a3-117">**bstrAllowedSourceIDs**</span></span>
</dt> <dd>

<span data-ttu-id="748a3-118">Specifica le origini del contenuto protetto da includere nella ricerca di licenze.</span><span class="sxs-lookup"><span data-stu-id="748a3-118">Specifies the sources of protected content to include in the license search.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="748a3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="748a3-119">Remarks</span></span>

<span data-ttu-id="748a3-120">Questa struttura viene utilizzata dal metodo [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="748a3-120">This structure is used by the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="748a3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="748a3-121">Requirements</span></span>



| <span data-ttu-id="748a3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="748a3-122">Requirement</span></span> | <span data-ttu-id="748a3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="748a3-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="748a3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="748a3-124">Header</span></span><br/> | <dl> <span data-ttu-id="748a3-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="748a3-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="748a3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="748a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="748a3-127">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="748a3-127">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





