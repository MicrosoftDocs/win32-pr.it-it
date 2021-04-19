---
description: Restituisce l'oggetto EKU utilizzato per compilare l'oggetto catena.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Metodo CertificateStatus. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324845"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="4d478-103">Metodo CertificateStatus. EKU</span><span class="sxs-lookup"><span data-stu-id="4d478-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="4d478-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4d478-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4d478-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4d478-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4d478-106">Il metodo **EKU** restituisce l'oggetto [**EKU**](eku.md) usato per compilare l'oggetto [**catena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="4d478-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d478-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d478-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="4d478-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d478-108">Parameters</span></span>

<span data-ttu-id="4d478-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4d478-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d478-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d478-110">Return value</span></span>

<span data-ttu-id="4d478-111">Questo metodo restituisce un oggetto [**EKU**](eku.md) che indica l'impostazione di utilizzo chiavi avanzato del [*certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4d478-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="4d478-112">L'impostazione EKU stabilisce un utilizzo valido del certificato.</span><span class="sxs-lookup"><span data-stu-id="4d478-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="4d478-113">Per ogni certificato è possibile impostare solo un singolo oggetto **EKU** .</span><span class="sxs-lookup"><span data-stu-id="4d478-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d478-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d478-114">Remarks</span></span>

<span data-ttu-id="4d478-115">Il metodo [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) fornisce la stessa funzionalità di questo metodo, ma consente di specificare molte impostazioni anziché una sola.</span><span class="sxs-lookup"><span data-stu-id="4d478-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="4d478-116">Se la raccolta [**OID**](oids.md) restituita dal metodo **ApplicationPolicies** contiene uno o più oggetti [**OID**](oid.md) , l'oggetto [**EKU**](eku.md) restituito da questo metodo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4d478-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="4d478-117">Usare il metodo **ApplicationPolicies** anziché questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4d478-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d478-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d478-118">Requirements</span></span>



| <span data-ttu-id="4d478-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d478-119">Requirement</span></span> | <span data-ttu-id="4d478-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4d478-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d478-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d478-121">End of client support</span></span><br/> | <span data-ttu-id="4d478-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d478-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d478-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4d478-123">End of server support</span></span><br/> | <span data-ttu-id="4d478-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d478-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d478-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4d478-125">Redistributable</span></span><br/>       | <span data-ttu-id="4d478-126">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d478-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4d478-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d478-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4d478-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d478-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d478-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d478-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d478-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="4d478-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="4d478-131">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="4d478-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4d478-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="4d478-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
