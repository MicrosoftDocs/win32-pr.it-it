---
description: Recupera l'OID del criterio. Si tratta della proprietà predefinita.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Proprietà PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324842"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="d2a84-104">Proprietà PolicyInformation. OID</span><span class="sxs-lookup"><span data-stu-id="d2a84-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="d2a84-105">\[La proprietà **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d2a84-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d2a84-106">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="d2a84-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="d2a84-107">La proprietà **OID** recupera l'OID del criterio.</span><span class="sxs-lookup"><span data-stu-id="d2a84-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="d2a84-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="d2a84-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a84-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a84-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="d2a84-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d2a84-110">Property value</span></span>

<span data-ttu-id="d2a84-111">Identificatore di oggetto del criterio come oggetto [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a84-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a84-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a84-112">Requirements</span></span>



| <span data-ttu-id="d2a84-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a84-113">Requirement</span></span> | <span data-ttu-id="d2a84-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a84-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a84-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d2a84-115">Redistributable</span></span><br/> | <span data-ttu-id="d2a84-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2a84-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d2a84-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d2a84-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="d2a84-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a84-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a84-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a84-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="d2a84-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
