---
description: Definisce i nomi di utilizzo chiavi estesi in base alla posizione in cui possono essere utilizzati.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumerazione CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328131"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="8da31-103">\_Enumerazione EKU di CAPICOM</span><span class="sxs-lookup"><span data-stu-id="8da31-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="8da31-104">Il tipo di enumerazione **\_ EKU CAPICOM** definisce i nomi di utilizzo chiavi estesi in base alla posizione in cui possono essere utilizzati.</span><span class="sxs-lookup"><span data-stu-id="8da31-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="8da31-105">Membri</span><span class="sxs-lookup"><span data-stu-id="8da31-105">Members</span></span>



| <span data-ttu-id="8da31-106">Membro</span><span class="sxs-lookup"><span data-stu-id="8da31-106">Member</span></span>                                     | <span data-ttu-id="8da31-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8da31-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="8da31-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8da31-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="8da31-109">**\_altro EKU di CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8da31-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="8da31-110">Il certificato ha usi definiti nei criteri locali.</span><span class="sxs-lookup"><span data-stu-id="8da31-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="8da31-111">Viene usato se l'EKU necessario non è predefinito e il valore OID deve essere impostato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8da31-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="8da31-112">0</span><span class="sxs-lookup"><span data-stu-id="8da31-112">0</span></span>     |
| <span data-ttu-id="8da31-113">**\_ \_ autenticazione server EKU CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8da31-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="8da31-114">Il certificato può essere usato per autenticare un server.</span><span class="sxs-lookup"><span data-stu-id="8da31-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="8da31-115">1</span><span class="sxs-lookup"><span data-stu-id="8da31-115">1</span></span>     |
| <span data-ttu-id="8da31-116">**\_ \_ autenticazione client EKU CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8da31-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="8da31-117">Il certificato può essere usato per autenticare un client.</span><span class="sxs-lookup"><span data-stu-id="8da31-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="8da31-118">2</span><span class="sxs-lookup"><span data-stu-id="8da31-118">2</span></span>     |
| <span data-ttu-id="8da31-119">**\_firma del codice EKU \_ di \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="8da31-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="8da31-120">Il certificato può essere usato per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="8da31-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="8da31-121">3</span><span class="sxs-lookup"><span data-stu-id="8da31-121">3</span></span>     |
| <span data-ttu-id="8da31-122">**\_ \_ protezione della posta elettronica EKU di CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8da31-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="8da31-123">Il certificato può essere usato per la protezione della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="8da31-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="8da31-124">4</span><span class="sxs-lookup"><span data-stu-id="8da31-124">4</span></span>     |
| <span data-ttu-id="8da31-125">**\_ \_ accesso smart card EKU CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="8da31-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="8da31-126">È possibile utilizzare il certificato per l'accesso con smart card.</span><span class="sxs-lookup"><span data-stu-id="8da31-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="8da31-127">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="8da31-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="8da31-128">5</span><span class="sxs-lookup"><span data-stu-id="8da31-128">5</span></span>     |
| <span data-ttu-id="8da31-129">**\_crittografia EKU del \_ \_ file \_ System per CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="8da31-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="8da31-130">Il certificato può essere usato per EFS.</span><span class="sxs-lookup"><span data-stu-id="8da31-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="8da31-131">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="8da31-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="8da31-132">6</span><span class="sxs-lookup"><span data-stu-id="8da31-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="8da31-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="8da31-133">Remarks</span></span>

<span data-ttu-id="8da31-134">Il tipo di enumerazione **\_ EKU CAPICOM** viene usato dall' [**EKU. Proprietà Name**](eku-name.md) .</span><span class="sxs-lookup"><span data-stu-id="8da31-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da31-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8da31-135">Requirements</span></span>



| <span data-ttu-id="8da31-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da31-136">Requirement</span></span> | <span data-ttu-id="8da31-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8da31-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8da31-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8da31-138">Redistributable</span></span><br/> | <span data-ttu-id="8da31-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="8da31-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="8da31-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8da31-140">Header</span></span><br/>          | <dl> <span data-ttu-id="8da31-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da31-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




