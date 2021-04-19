---
description: Restituisce una raccolta OID che rappresenta i criteri dell'applicazione utilizzati per creare l'oggetto catena.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. ApplicationPolicies, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326151"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="fa9d6-103">CertificateStatus. ApplicationPolicies, metodo</span><span class="sxs-lookup"><span data-stu-id="fa9d6-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="fa9d6-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fa9d6-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fa9d6-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fa9d6-106">Il metodo **ApplicationPolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri dell'applicazione utilizzati per creare l'oggetto [**catena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="fa9d6-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9d6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa9d6-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="fa9d6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa9d6-108">Parameters</span></span>

<span data-ttu-id="fa9d6-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa9d6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa9d6-110">Return value</span></span>

<span data-ttu-id="fa9d6-111">Raccolta [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="fa9d6-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="fa9d6-112">Ogni oggetto [**OID**](oid.md) della raccolta rappresenta un OID dei criteri dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa9d6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa9d6-113">Remarks</span></span>

<span data-ttu-id="fa9d6-114">Aggiungere i criteri dell'applicazione OID alla raccolta per specificare i criteri dell'applicazione da usare per compilare la catena di certificati attendibili.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="fa9d6-115">Se la raccolta contiene almeno un oggetto [**OID**](oid.md) , l'oggetto [**EKU**](eku.md) restituito dal metodo [**CertificateStatus. EKU**](certificatestatus-eku.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9d6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa9d6-116">Requirements</span></span>



| <span data-ttu-id="fa9d6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa9d6-117">Requirement</span></span> | <span data-ttu-id="fa9d6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fa9d6-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9d6-119">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fa9d6-119">End of client support</span></span><br/> | <span data-ttu-id="fa9d6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa9d6-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fa9d6-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fa9d6-121">End of server support</span></span><br/> | <span data-ttu-id="fa9d6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa9d6-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fa9d6-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fa9d6-123">Redistributable</span></span><br/>       | <span data-ttu-id="fa9d6-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa9d6-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fa9d6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa9d6-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fa9d6-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa9d6-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
