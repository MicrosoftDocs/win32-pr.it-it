---
description: La proprietà Certificates recupera una raccolta di certificati che rappresenta i certificati nella catena. Si tratta della proprietà predefinita.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'Proprietà IChain2:: Certificates'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327094"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="738c2-104">Proprietà IChain2:: Certificates</span><span class="sxs-lookup"><span data-stu-id="738c2-104">IChain2::Certificates property</span></span>

<span data-ttu-id="738c2-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="738c2-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="738c2-106">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="738c2-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="738c2-107">La proprietà **Certificates** recupera una raccolta di [**certificati**](certificates.md) che rappresenta i certificati nella catena.</span><span class="sxs-lookup"><span data-stu-id="738c2-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="738c2-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="738c2-108">This is the default property.</span></span>

<span data-ttu-id="738c2-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="738c2-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="738c2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="738c2-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="738c2-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="738c2-111">Property value</span></span>

<span data-ttu-id="738c2-112">Raccolta di [**certificati**](certificates.md) utilizzata per recuperare informazioni su ogni certificato nella catena.</span><span class="sxs-lookup"><span data-stu-id="738c2-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="738c2-113">Il primo certificato della raccolta restituita, **Certificates. Item**(1), è il certificato finale della catena.</span><span class="sxs-lookup"><span data-stu-id="738c2-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="738c2-114">L'ultimo certificato della raccolta, **Certificates. Item**(**Certificates. Count**), è il [*certificato radice*](../secgloss/r-gly.md) della catena.</span><span class="sxs-lookup"><span data-stu-id="738c2-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="738c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="738c2-115">Requirements</span></span>



| <span data-ttu-id="738c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="738c2-116">Requirement</span></span> | <span data-ttu-id="738c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="738c2-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="738c2-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="738c2-118">End of client support</span></span><br/> | <span data-ttu-id="738c2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="738c2-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="738c2-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="738c2-120">End of server support</span></span><br/> | <span data-ttu-id="738c2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="738c2-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="738c2-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="738c2-122">Redistributable</span></span><br/>       | <span data-ttu-id="738c2-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="738c2-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="738c2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="738c2-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="738c2-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738c2-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
