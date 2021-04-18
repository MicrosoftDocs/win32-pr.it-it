---
description: Indica cosa viene verificato quando viene verificata una firma digitale.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Enumerazione CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331053"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="52c79-103">\_Enumerazione del flag di \_ Verifica dei dati firmati capicol \_ \_</span><span class="sxs-lookup"><span data-stu-id="52c79-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="52c79-104">L'enumerazione del **flag CApicol \_ signed \_ data \_ Verify \_** indica cosa viene verificato quando viene verificata una [*firma digitale*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="52c79-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="52c79-105">Membri</span><span class="sxs-lookup"><span data-stu-id="52c79-105">Members</span></span>



| <span data-ttu-id="52c79-106">Membro</span><span class="sxs-lookup"><span data-stu-id="52c79-106">Member</span></span>                                           | <span data-ttu-id="52c79-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52c79-107">Description</span></span>                                                                                                 | <span data-ttu-id="52c79-108">Valore</span><span class="sxs-lookup"><span data-stu-id="52c79-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="52c79-109">**CAPICOM \_ verificare solo la \_ firma \_**</span><span class="sxs-lookup"><span data-stu-id="52c79-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="52c79-110">Viene controllata solo la firma.</span><span class="sxs-lookup"><span data-stu-id="52c79-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="52c79-111">0</span><span class="sxs-lookup"><span data-stu-id="52c79-111">0</span></span>     |
| <span data-ttu-id="52c79-112">**\_verificare la \_ firma e il \_ \_ certificato di CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="52c79-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="52c79-113">Vengono controllati sia la firma che la validità del certificato utilizzato per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="52c79-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="52c79-114">1</span><span class="sxs-lookup"><span data-stu-id="52c79-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="52c79-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c79-115">Requirements</span></span>



| <span data-ttu-id="52c79-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c79-116">Requirement</span></span> | <span data-ttu-id="52c79-117">Valore</span><span class="sxs-lookup"><span data-stu-id="52c79-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52c79-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="52c79-118">Redistributable</span></span><br/> | <span data-ttu-id="52c79-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="52c79-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="52c79-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52c79-120">Header</span></span><br/>          | <dl> <span data-ttu-id="52c79-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c79-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
