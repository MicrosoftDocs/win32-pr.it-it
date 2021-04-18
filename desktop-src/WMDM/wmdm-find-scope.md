---
title: Enumerazione WMDM_FIND_SCOPE
description: Il \_ \_ tipo di enumerazione WMDM Find scope definisce l'ambito dell'oggetto di archiviazione.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- Enumerazione WMDM_FIND_SCOPE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325012"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="40fea-104">\_Enumerazione WMDM Find \_ scope</span><span class="sxs-lookup"><span data-stu-id="40fea-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="40fea-105">Il tipo di enumerazione **WMDM \_ Find \_ scope** definisce l'ambito dell'oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="40fea-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40fea-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="40fea-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="40fea-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="40fea-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ trova \_ ambito \_ globale**</span><span class="sxs-lookup"><span data-stu-id="40fea-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="40fea-109">Ricerca dell'oggetto corrispondente in qualsiasi punto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40fea-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="40fea-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ trova \_ ambito \_ elementi figlio immediati \_**</span><span class="sxs-lookup"><span data-stu-id="40fea-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="40fea-111">Ricerca dell'oggetto corrispondente all'interno di questa risorsa di archiviazione e dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="40fea-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40fea-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40fea-112">Requirements</span></span>



| <span data-ttu-id="40fea-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="40fea-113">Requirement</span></span> | <span data-ttu-id="40fea-114">Valore</span><span class="sxs-lookup"><span data-stu-id="40fea-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40fea-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40fea-115">Header</span></span><br/> | <dl> <span data-ttu-id="40fea-116"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="40fea-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40fea-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40fea-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fea-118">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="40fea-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





