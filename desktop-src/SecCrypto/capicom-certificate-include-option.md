---
description: Definisce quali certificati di una catena vengono salvati.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumerazione CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329737"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="07d34-103">\_ \_ Enumerazione dell'opzione Includi certificato capicol \_</span><span class="sxs-lookup"><span data-stu-id="07d34-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="07d34-104">Il tipo di enumerazione dell' **\_ \_ \_ opzione Includi certificato CAPICOM** definisce i certificati in una catena salvati.</span><span class="sxs-lookup"><span data-stu-id="07d34-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="07d34-105">Questo tipo di enumerazione è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="07d34-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="07d34-106">Membri</span><span class="sxs-lookup"><span data-stu-id="07d34-106">Members</span></span>



| <span data-ttu-id="07d34-107">Membro</span><span class="sxs-lookup"><span data-stu-id="07d34-107">Member</span></span>                                                 | <span data-ttu-id="07d34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d34-108">Description</span></span>                                                                           | <span data-ttu-id="07d34-109">Valore</span><span class="sxs-lookup"><span data-stu-id="07d34-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="07d34-110">**il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice**</span><span class="sxs-lookup"><span data-stu-id="07d34-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="07d34-111">Salva tutti i certificati nella catena con l'eccezione dell'entità radice.</span><span class="sxs-lookup"><span data-stu-id="07d34-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="07d34-112">0</span><span class="sxs-lookup"><span data-stu-id="07d34-112">0</span></span>     |
| <span data-ttu-id="07d34-113">**il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**</span><span class="sxs-lookup"><span data-stu-id="07d34-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="07d34-114">Salva la catena di certificati completa.</span><span class="sxs-lookup"><span data-stu-id="07d34-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="07d34-115">1</span><span class="sxs-lookup"><span data-stu-id="07d34-115">1</span></span>     |
| <span data-ttu-id="07d34-116">**il certificato capicol \_ \_ include \_ \_ solo entità finale \_**</span><span class="sxs-lookup"><span data-stu-id="07d34-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="07d34-117">Salva solo il certificato dell'entità finale.</span><span class="sxs-lookup"><span data-stu-id="07d34-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="07d34-118">2</span><span class="sxs-lookup"><span data-stu-id="07d34-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="07d34-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="07d34-119">Remarks</span></span>

<span data-ttu-id="07d34-120">Il tipo di enumerazione dell' **\_ \_ \_ opzione di inclusione del certificato CAPICOM** viene utilizzato dal metodo [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="07d34-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d34-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d34-121">Requirements</span></span>



| <span data-ttu-id="07d34-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d34-122">Requirement</span></span> | <span data-ttu-id="07d34-123">Valore</span><span class="sxs-lookup"><span data-stu-id="07d34-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07d34-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="07d34-124">Redistributable</span></span><br/> | <span data-ttu-id="07d34-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="07d34-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="07d34-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07d34-126">Header</span></span><br/>          | <dl> <span data-ttu-id="07d34-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d34-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




