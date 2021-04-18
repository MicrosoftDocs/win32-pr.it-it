---
description: Recupera la raccolta di certificati associata all'oggetto SignedData. Dopo essere stati recuperati, è possibile enumerare i singoli oggetti certificato della raccolta.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Proprietà SignedData. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327894"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="ffb31-104">Proprietà SignedData. Certificates</span><span class="sxs-lookup"><span data-stu-id="ffb31-104">SignedData.Certificates property</span></span>

<span data-ttu-id="ffb31-105">\[La proprietà **Certificates** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ffb31-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ffb31-106">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ffb31-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ffb31-107">La proprietà **Certificates** recupera la raccolta di [**certificati**](certificates.md) associata all'oggetto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb31-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="ffb31-108">Dopo essere stati recuperati, è possibile enumerare i singoli oggetti [**certificato**](certificate.md) della raccolta.</span><span class="sxs-lookup"><span data-stu-id="ffb31-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb31-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffb31-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="ffb31-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ffb31-110">Property value</span></span>

<span data-ttu-id="ffb31-111">Raccolta di [**certificati**](certificates.md) associata all'oggetto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb31-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb31-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffb31-112">Requirements</span></span>



| <span data-ttu-id="ffb31-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb31-113">Requirement</span></span> | <span data-ttu-id="ffb31-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ffb31-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb31-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ffb31-115">Redistributable</span></span><br/> | <span data-ttu-id="ffb31-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ffb31-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ffb31-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ffb31-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="ffb31-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffb31-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb31-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffb31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb31-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="ffb31-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
