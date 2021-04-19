---
description: Indica il tipo di codifica utilizzato.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumerazione CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332160"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="be1c8-103">\_Enumerazione del tipo di codifica CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="be1c8-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="be1c8-104">Il tipo di enumerazione del **\_ \_ tipo di codifica capicol** indica il tipo di codifica utilizzato.</span><span class="sxs-lookup"><span data-stu-id="be1c8-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="be1c8-105">Membri</span><span class="sxs-lookup"><span data-stu-id="be1c8-105">Members</span></span>



| <span data-ttu-id="be1c8-106">Membro</span><span class="sxs-lookup"><span data-stu-id="be1c8-106">Member</span></span>                      | <span data-ttu-id="be1c8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be1c8-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="be1c8-108">Valore</span><span class="sxs-lookup"><span data-stu-id="be1c8-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="be1c8-109">**CAPICOM \_ Encode \_ any**</span><span class="sxs-lookup"><span data-stu-id="be1c8-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="be1c8-110">I dati vengono salvati come stringa con codifica Base64 o come sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="be1c8-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="be1c8-111">Questo tipo di codifica viene utilizzato solo per i dati di input con un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="be1c8-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="be1c8-112">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="be1c8-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="be1c8-113">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="be1c8-113">0xffffffff</span></span> |
| <span data-ttu-id="be1c8-114">**\_Codifica Base64 per CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="be1c8-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="be1c8-115">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="be1c8-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="be1c8-116">0</span><span class="sxs-lookup"><span data-stu-id="be1c8-116">0</span></span>          |
| <span data-ttu-id="be1c8-117">**\_codificare il \_ file binario di CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="be1c8-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="be1c8-118">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="be1c8-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="be1c8-119">1</span><span class="sxs-lookup"><span data-stu-id="be1c8-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="be1c8-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="be1c8-120">Remarks</span></span>

<span data-ttu-id="be1c8-121">Questo tipo di enumerazione viene usato dai metodi e dalle proprietà di CAPICOM seguenti:</span><span class="sxs-lookup"><span data-stu-id="be1c8-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="be1c8-122">Metodo [**Certificate. Export**](certificate-export.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="be1c8-123">Proprietà [**EncodedData. Value**](encodeddata-value.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="be1c8-124">Metodo [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="be1c8-125">Metodo [**EnvelopedData. Encrypt**](envelopeddata-encrypt.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="be1c8-126">Proprietà [**ExtendedProperty. Value**](extendedproperty-value.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="be1c8-127">Metodo [**SignedData. Sign**](signeddata-sign.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="be1c8-128">Metodo [**SignedData. cosign**](signeddata-cosign.md)</span><span class="sxs-lookup"><span data-stu-id="be1c8-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="be1c8-129">[**Store. Export**](store-export.md) (metodo)</span><span class="sxs-lookup"><span data-stu-id="be1c8-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="be1c8-130">[**Utilities. GetRandom,**](utilities-getrandom.md) metodo</span><span class="sxs-lookup"><span data-stu-id="be1c8-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="be1c8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be1c8-131">Requirements</span></span>



| <span data-ttu-id="be1c8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="be1c8-132">Requirement</span></span> | <span data-ttu-id="be1c8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="be1c8-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be1c8-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="be1c8-134">Redistributable</span></span><br/> | <span data-ttu-id="be1c8-135">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="be1c8-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="be1c8-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be1c8-136">Header</span></span><br/>          | <dl> <span data-ttu-id="be1c8-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="be1c8-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




