---
description: Restituisce la raccolta EKU per il certificato.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Proprietà ExtendedKeyUsage. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324239"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="366df-103">Proprietà ExtendedKeyUsage. EKU</span><span class="sxs-lookup"><span data-stu-id="366df-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="366df-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="366df-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="366df-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="366df-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="366df-106">La proprietà **EKU** restituisce la raccolta [**EKU**](ekus.md) per il certificato.</span><span class="sxs-lookup"><span data-stu-id="366df-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="366df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="366df-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="366df-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="366df-108">Property value</span></span>

<span data-ttu-id="366df-109">Raccolta [**EKU**](ekus.md) che contiene gli oggetti [**EKU**](eku.md) per il certificato.</span><span class="sxs-lookup"><span data-stu-id="366df-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="366df-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="366df-110">Requirements</span></span>



| <span data-ttu-id="366df-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="366df-111">Requirement</span></span> | <span data-ttu-id="366df-112">Valore</span><span class="sxs-lookup"><span data-stu-id="366df-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="366df-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="366df-113">End of client support</span></span><br/> | <span data-ttu-id="366df-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="366df-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="366df-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="366df-115">End of server support</span></span><br/> | <span data-ttu-id="366df-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="366df-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="366df-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="366df-117">Redistributable</span></span><br/>       | <span data-ttu-id="366df-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="366df-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="366df-119">DLL</span><span class="sxs-lookup"><span data-stu-id="366df-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="366df-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="366df-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="366df-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="366df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366df-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="366df-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
