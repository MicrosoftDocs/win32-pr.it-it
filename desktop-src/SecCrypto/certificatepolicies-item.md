---
description: Recupera l'oggetto PolicyInformation che rappresenta i criteri indicizzati. Si tratta della proprietà predefinita.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: Proprietà CertificatePolicies. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332841"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="c4974-104">Proprietà CertificatePolicies. Item</span><span class="sxs-lookup"><span data-stu-id="c4974-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="c4974-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c4974-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c4974-106">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="c4974-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="c4974-107">La proprietà **Item** recupera l'oggetto [**PolicyInformation**](policyinformation.md) che rappresenta i criteri indicizzati.</span><span class="sxs-lookup"><span data-stu-id="c4974-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="c4974-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="c4974-108">This is the default property.</span></span>

<span data-ttu-id="c4974-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c4974-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4974-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4974-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="c4974-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c4974-111">Property value</span></span>

<span data-ttu-id="c4974-112">Oggetto [**PolicyInformation**](policyinformation.md) che rappresenta i criteri indicizzati.</span><span class="sxs-lookup"><span data-stu-id="c4974-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4974-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4974-113">Requirements</span></span>



| <span data-ttu-id="c4974-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4974-114">Requirement</span></span> | <span data-ttu-id="c4974-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c4974-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4974-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c4974-116">End of client support</span></span><br/> | <span data-ttu-id="c4974-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4974-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4974-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c4974-118">End of server support</span></span><br/> | <span data-ttu-id="c4974-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4974-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4974-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c4974-120">Redistributable</span></span><br/>       | <span data-ttu-id="c4974-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4974-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c4974-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c4974-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c4974-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4974-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
