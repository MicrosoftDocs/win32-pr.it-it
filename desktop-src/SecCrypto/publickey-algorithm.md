---
description: La proprietà Algorithm recupera l'oggetto OID che identifica l'algoritmo utilizzato dalla chiave pubblica. Si tratta della proprietà predefinita.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Proprietà PublicKey. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329331"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="60b6b-104">Proprietà PublicKey. Algorithm</span><span class="sxs-lookup"><span data-stu-id="60b6b-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="60b6b-105">\[La proprietà **algoritmo** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="60b6b-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60b6b-106">Usare invece la [**Proprietà X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="60b6b-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="60b6b-107">La proprietà **Algorithm** recupera l'oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="60b6b-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="60b6b-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="60b6b-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b6b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60b6b-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="60b6b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="60b6b-110">Property value</span></span>

<span data-ttu-id="60b6b-111">Oggetto [**OID**](oid.md) che identifica l'algoritmo utilizzato dalla chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="60b6b-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b6b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60b6b-112">Requirements</span></span>



| <span data-ttu-id="60b6b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b6b-113">Requirement</span></span> | <span data-ttu-id="60b6b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="60b6b-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b6b-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="60b6b-115">Redistributable</span></span><br/> | <span data-ttu-id="60b6b-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="60b6b-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="60b6b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="60b6b-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="60b6b-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b6b-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b6b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60b6b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b6b-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="60b6b-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
