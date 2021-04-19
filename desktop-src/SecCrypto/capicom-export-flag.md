---
description: Il \_ tipo di enumerazione del flag di esportazione CAPICOM \_ definisce se eventuali errori di esportazione della chiave privata vengono ignorati.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Enumerazione CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327647"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="3f071-103">\_Enumerazione del flag di esportazione CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="3f071-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="3f071-104">Il tipo di enumerazione del **\_ \_ flag di esportazione CAPICOM** definisce se eventuali errori di esportazione della chiave privata vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="3f071-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="3f071-105">Membri</span><span class="sxs-lookup"><span data-stu-id="3f071-105">Members</span></span>



| <span data-ttu-id="3f071-106">Membro</span><span class="sxs-lookup"><span data-stu-id="3f071-106">Member</span></span>                                                            | <span data-ttu-id="3f071-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f071-107">Description</span></span>                                               | <span data-ttu-id="3f071-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3f071-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="3f071-109">**impostazione predefinita per l'esportazione di CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f071-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="3f071-110">Eventuali errori di esportazione della chiave privata non vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="3f071-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="3f071-111">0</span><span class="sxs-lookup"><span data-stu-id="3f071-111">0</span></span>     |
| <span data-ttu-id="3f071-112">**errore di esportazione di CAPICOM \_ \_ Ignora \_ \_ chiave privata \_ non \_ esportabile \_**</span><span class="sxs-lookup"><span data-stu-id="3f071-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="3f071-113">Eventuali errori di esportazione della chiave privata vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="3f071-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="3f071-114">1</span><span class="sxs-lookup"><span data-stu-id="3f071-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="3f071-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f071-115">Remarks</span></span>

<span data-ttu-id="3f071-116">Il \_ \_ tipo di enumerazione del flag di esportazione CAPICOM viene utilizzato dal metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="3f071-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="3f071-117">**Certificati. Salva**</span><span class="sxs-lookup"><span data-stu-id="3f071-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="3f071-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f071-118">Requirements</span></span>



| <span data-ttu-id="3f071-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f071-119">Requirement</span></span> | <span data-ttu-id="3f071-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3f071-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f071-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3f071-121">Redistributable</span></span><br/> | <span data-ttu-id="3f071-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f071-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="3f071-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f071-123">Header</span></span><br/>          | <dl> <span data-ttu-id="3f071-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f071-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




