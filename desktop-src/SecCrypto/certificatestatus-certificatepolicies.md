---
description: Restituisce una raccolta OID che rappresenta i criteri del certificato utilizzati per creare l'oggetto catena.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. CertificatePolicies, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327637"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="ebd1f-103">CertificateStatus. CertificatePolicies, metodo</span><span class="sxs-lookup"><span data-stu-id="ebd1f-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="ebd1f-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ebd1f-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ebd1f-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ebd1f-106">Il metodo **CertificatePolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri del certificato utilizzati per creare l'oggetto [**Chain**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd1f-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd1f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebd1f-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="ebd1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebd1f-108">Parameters</span></span>

<span data-ttu-id="ebd1f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebd1f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebd1f-110">Return value</span></span>

<span data-ttu-id="ebd1f-111">Raccolta [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="ebd1f-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="ebd1f-112">Ogni oggetto [**OID**](oid.md) della raccolta rappresenta un OID del criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd1f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebd1f-113">Remarks</span></span>

<span data-ttu-id="ebd1f-114">Aggiungere i criteri di certificato OID alla raccolta per specificare i criteri dei certificati che devono essere usati per compilare la catena di certificati attendibili.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd1f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebd1f-115">Requirements</span></span>



| <span data-ttu-id="ebd1f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd1f-116">Requirement</span></span> | <span data-ttu-id="ebd1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ebd1f-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd1f-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ebd1f-118">End of client support</span></span><br/> | <span data-ttu-id="ebd1f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebd1f-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ebd1f-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ebd1f-120">End of server support</span></span><br/> | <span data-ttu-id="ebd1f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebd1f-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebd1f-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ebd1f-122">Redistributable</span></span><br/>       | <span data-ttu-id="ebd1f-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebd1f-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ebd1f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd1f-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ebd1f-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd1f-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
