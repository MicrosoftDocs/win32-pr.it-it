---
description: Recupera il numero di oggetti PolicyInformation nell'insieme.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Proprietà CertificatePolicies. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333020"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="d4e89-103">Proprietà CertificatePolicies. Count</span><span class="sxs-lookup"><span data-stu-id="d4e89-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="d4e89-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4e89-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d4e89-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="d4e89-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="d4e89-106">La proprietà **count** Recupera il numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="d4e89-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="d4e89-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d4e89-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e89-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4e89-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="d4e89-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d4e89-109">Property value</span></span>

<span data-ttu-id="d4e89-110">Numero di oggetti [**PolicyInformation**](policyinformation.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="d4e89-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="d4e89-111">Ogni oggetto **PolicyInformation** rappresenta un singolo criterio del certificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4e89-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4e89-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4e89-112">Remarks</span></span>

<span data-ttu-id="d4e89-113">La proprietà **count** può essere usata per specificare l'ultimo oggetto [**PolicyInformation**](policyinformation.md) nella raccolta durante il recupero di un oggetto **PolicyInformation** specifico usando la proprietà [**CertificatePolicies. Item**](certificatepolicies-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e89-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e89-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4e89-114">Requirements</span></span>



| <span data-ttu-id="d4e89-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e89-115">Requirement</span></span> | <span data-ttu-id="d4e89-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4e89-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e89-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d4e89-117">End of client support</span></span><br/> | <span data-ttu-id="d4e89-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4e89-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d4e89-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d4e89-119">End of server support</span></span><br/> | <span data-ttu-id="d4e89-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4e89-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d4e89-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d4e89-121">Redistributable</span></span><br/>       | <span data-ttu-id="d4e89-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4e89-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d4e89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d4e89-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d4e89-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4e89-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
