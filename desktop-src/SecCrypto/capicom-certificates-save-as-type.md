---
description: Definisce il formato di un file contenente le informazioni sui certificati.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumerazione CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328133"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a><span data-ttu-id="49855-103">\_Enumerazione dei certificati CAPICOM \_ Salva \_ come \_ tipo</span><span class="sxs-lookup"><span data-stu-id="49855-103">CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="49855-104">Il tipo di enumerazione dei **certificati di capico \_ \_ \_ , \_** che definisce il formato di un file contenente le informazioni sui certificati.</span><span class="sxs-lookup"><span data-stu-id="49855-104">The **CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificates information.</span></span> <span data-ttu-id="49855-105">Questo tipo di enumerazione è stato introdotto da capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="49855-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="49855-106">Membri</span><span class="sxs-lookup"><span data-stu-id="49855-106">Members</span></span>



| <span data-ttu-id="49855-107">Membro</span><span class="sxs-lookup"><span data-stu-id="49855-107">Member</span></span>                                          | <span data-ttu-id="49855-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49855-108">Description</span></span>                                          | <span data-ttu-id="49855-109">Valore</span><span class="sxs-lookup"><span data-stu-id="49855-109">Value</span></span> |
|-------------------------------------------------|------------------------------------------------------|-------|
| <span data-ttu-id="49855-110">**i certificati CAPICOM \_ vengono \_ salvati \_ come \_ serializzati**</span><span class="sxs-lookup"><span data-stu-id="49855-110">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</span></span> | <span data-ttu-id="49855-111">I certificati salvati vengono serializzati.</span><span class="sxs-lookup"><span data-stu-id="49855-111">The saved certificates are serialized.</span></span><br/>    | <span data-ttu-id="49855-112">0</span><span class="sxs-lookup"><span data-stu-id="49855-112">0</span></span>     |
| <span data-ttu-id="49855-113">**I certificati CAPICOM \_ vengono \_ salvati \_ come \_ PKCS7**</span><span class="sxs-lookup"><span data-stu-id="49855-113">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</span></span>      | <span data-ttu-id="49855-114">I certificati vengono salvati come PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="49855-114">The certificates are saved as a PKCS \#7.</span></span><br/> | <span data-ttu-id="49855-115">1</span><span class="sxs-lookup"><span data-stu-id="49855-115">1</span></span>     |
| <span data-ttu-id="49855-116">**\_certificati CAPICOM \_ Salva \_ come \_ PFX**</span><span class="sxs-lookup"><span data-stu-id="49855-116">**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</span></span>        | <span data-ttu-id="49855-117">I certificati vengono salvati come PFX.</span><span class="sxs-lookup"><span data-stu-id="49855-117">The certificates are saved as a PFX.</span></span><br/>      | <span data-ttu-id="49855-118">2</span><span class="sxs-lookup"><span data-stu-id="49855-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="49855-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="49855-119">Remarks</span></span>

<span data-ttu-id="49855-120">Il \_ tipo di enumerazione dei certificati capico \_ \_ \_ è usato dal metodo [**Certificates. Save**](certificates-save.md) .</span><span class="sxs-lookup"><span data-stu-id="49855-120">The CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE enumeration type is used by the [**Certificates.Save**](certificates-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="49855-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49855-121">Requirements</span></span>



| <span data-ttu-id="49855-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="49855-122">Requirement</span></span> | <span data-ttu-id="49855-123">Valore</span><span class="sxs-lookup"><span data-stu-id="49855-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49855-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="49855-124">Redistributable</span></span><br/> | <span data-ttu-id="49855-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="49855-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="49855-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49855-126">Header</span></span><br/>          | <dl> <span data-ttu-id="49855-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="49855-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




