---
description: Compila una catena di verifica del certificato da un certificato finale al certificato radice attendibile e restituisce un valore booleano che indica la validità complessiva della catena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Metodo IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323968"
---
# <a name="ichain2build-method"></a><span data-ttu-id="f7bdc-103">Metodo IChain2:: Build</span><span class="sxs-lookup"><span data-stu-id="f7bdc-103">IChain2::Build method</span></span>

<span data-ttu-id="f7bdc-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7bdc-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f7bdc-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f7bdc-106">Il metodo di **compilazione** compila una catena di verifica del certificato da un certificato finale al [*certificato radice*](../secgloss/r-gly.md) attendibile e restituisce un valore booleano che indica la validità complessiva della catena.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7bdc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7bdc-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="f7bdc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7bdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7bdc-109">*Certificato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f7bdc-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7bdc-110">Oggetto [**certificato**](certificate.md) che rappresenta il certificato finale sul quale deve essere compilata la catena di verifica.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7bdc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7bdc-111">Return value</span></span>

<span data-ttu-id="f7bdc-112">Valore booleano che indica la validità complessiva della catena.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="f7bdc-113">La validità complessiva si basa sui criteri di verifica della validità sul posto.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7bdc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7bdc-114">Remarks</span></span>

<span data-ttu-id="f7bdc-115">La catena viene compilata usando la proprietà [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , nonché i criteri di applicazione e di certificato specificati da un oggetto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f7bdc-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="f7bdc-116">La raccolta restituita è ordinata; il primo certificato della raccolta, **Certificates. Item**(1), è il certificato finale della catena.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="f7bdc-117">L'ultimo certificato della raccolta, **Certificates. Item**(**Certificates. Count**), è il [*certificato radice*](../secgloss/r-gly.md) della catena.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="f7bdc-118">**Certificates. Item**(0) rappresenta l'intera catena.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="f7bdc-119">Ogni volta che viene chiamato il metodo **chain. Build** , lo [*stato*](../secgloss/s-gly.md) dell'oggetto [**Chain**](chain.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="f7bdc-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7bdc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7bdc-120">Requirements</span></span>



| <span data-ttu-id="f7bdc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7bdc-121">Requirement</span></span> | <span data-ttu-id="f7bdc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f7bdc-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7bdc-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f7bdc-123">End of client support</span></span><br/> | <span data-ttu-id="f7bdc-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7bdc-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7bdc-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f7bdc-125">End of server support</span></span><br/> | <span data-ttu-id="f7bdc-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7bdc-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7bdc-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f7bdc-127">Redistributable</span></span><br/>       | <span data-ttu-id="f7bdc-128">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7bdc-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7bdc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f7bdc-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7bdc-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7bdc-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7bdc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7bdc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7bdc-132">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="f7bdc-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f7bdc-133">**Catena**</span><span class="sxs-lookup"><span data-stu-id="f7bdc-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
