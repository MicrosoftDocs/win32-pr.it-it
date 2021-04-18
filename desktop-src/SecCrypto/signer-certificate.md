---
description: Imposta o recupera l'oggetto certificato che rappresenta il certificato di un firmatario dei dati.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Proprietà Signer. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324461"
---
# <a name="signercertificate-property"></a><span data-ttu-id="5c6a9-103">Proprietà Signer. Certificate</span><span class="sxs-lookup"><span data-stu-id="5c6a9-103">Signer.Certificate property</span></span>

<span data-ttu-id="5c6a9-104">\[La proprietà **certificato** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5c6a9-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5c6a9-105">Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5c6a9-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5c6a9-106">La proprietà **Certificate** imposta o recupera l'oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati.</span><span class="sxs-lookup"><span data-stu-id="5c6a9-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="5c6a9-107">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="5c6a9-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c6a9-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="5c6a9-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5c6a9-109">Property value</span></span>

<span data-ttu-id="5c6a9-110">Oggetto [**certificato**](certificate.md) che rappresenta il certificato di un firmatario dei dati.</span><span class="sxs-lookup"><span data-stu-id="5c6a9-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c6a9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c6a9-111">Remarks</span></span>

<span data-ttu-id="5c6a9-112">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c6a9-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c6a9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c6a9-113">Requirements</span></span>



| <span data-ttu-id="5c6a9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6a9-114">Requirement</span></span> | <span data-ttu-id="5c6a9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5c6a9-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6a9-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5c6a9-116">Redistributable</span></span><br/> | <span data-ttu-id="5c6a9-117">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c6a9-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5c6a9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5c6a9-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="5c6a9-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c6a9-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c6a9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c6a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6a9-121">**Firmatario**</span><span class="sxs-lookup"><span data-stu-id="5c6a9-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
