---
description: L' \_ enumerazione delle specifiche della chiave CAPICOM definisce le \_ specifiche principali.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: Enumerazione CAPICOM_KEY_SPEC (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327642"
---
# <a name="capicom_key_spec-enumeration"></a><span data-ttu-id="dd75a-103">\_Enumerazione delle specifiche della chiave CApicot \_</span><span class="sxs-lookup"><span data-stu-id="dd75a-103">CAPICOM\_KEY\_SPEC enumeration</span></span>

<span data-ttu-id="dd75a-104">L'enumerazione delle **\_ \_ specifiche della chiave CAPICOM** definisce le specifiche principali.</span><span class="sxs-lookup"><span data-stu-id="dd75a-104">The **CAPICOM\_KEY\_SPEC** enumeration defines key specifications.</span></span>

## <a name="members"></a><span data-ttu-id="dd75a-105">Membri</span><span class="sxs-lookup"><span data-stu-id="dd75a-105">Members</span></span>



| <span data-ttu-id="dd75a-106">Membro</span><span class="sxs-lookup"><span data-stu-id="dd75a-106">Member</span></span>                              | <span data-ttu-id="dd75a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd75a-107">Description</span></span>                                                | <span data-ttu-id="dd75a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="dd75a-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|-------|
| <span data-ttu-id="dd75a-109">**chiave per lo \_ scambio di chiavi di CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd75a-109">**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</span></span> | <span data-ttu-id="dd75a-110">La chiave può essere usata per la crittografia e la firma.</span><span class="sxs-lookup"><span data-stu-id="dd75a-110">The key can be used for encryption and signing.</span></span><br/> | <span data-ttu-id="dd75a-111">1</span><span class="sxs-lookup"><span data-stu-id="dd75a-111">1</span></span>     |
| <span data-ttu-id="dd75a-112">**firma della specifica della \_ chiave CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dd75a-112">**CAPICOM\_KEY\_SPEC\_SIGNATURE**</span></span>   | <span data-ttu-id="dd75a-113">La chiave può essere usata solo per la firma.</span><span class="sxs-lookup"><span data-stu-id="dd75a-113">The key can be used only for signing.</span></span><br/>           | <span data-ttu-id="dd75a-114">2</span><span class="sxs-lookup"><span data-stu-id="dd75a-114">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="dd75a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd75a-115">Remarks</span></span>

<span data-ttu-id="dd75a-116">L'enumerazione delle **\_ \_ specifiche della chiave CAPICOM** viene utilizzata dai metodi e dalle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd75a-116">The **CAPICOM\_KEY\_SPEC** enumeration is used by the following methods and properties:</span></span>

-   <span data-ttu-id="dd75a-117">Proprietà [**PrivateKey. dataspec**](privatekey-keyspec.md) .</span><span class="sxs-lookup"><span data-stu-id="dd75a-117">[**PrivateKey.KeySpec**](privatekey-keyspec.md) property.</span></span>
-   <span data-ttu-id="dd75a-118">Metodo [**PrivateKey. Open**](privatekey-open.md) .</span><span class="sxs-lookup"><span data-stu-id="dd75a-118">[**PrivateKey.Open**](privatekey-open.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd75a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd75a-119">Requirements</span></span>



| <span data-ttu-id="dd75a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd75a-120">Requirement</span></span> | <span data-ttu-id="dd75a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dd75a-121">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd75a-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="dd75a-122">Redistributable</span></span><br/> | <span data-ttu-id="dd75a-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd75a-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="dd75a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd75a-124">Header</span></span><br/>          | <dl> <span data-ttu-id="dd75a-125"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd75a-125"><dt>Capicom.h</dt></span></span> </dl> |



 

 




