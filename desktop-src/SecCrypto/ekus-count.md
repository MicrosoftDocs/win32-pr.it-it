---
description: Recupera il numero di oggetti EKU nell'insieme.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Proprietà EKU. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330911"
---
# <a name="ekuscount-property"></a><span data-ttu-id="fb9a6-103">Proprietà EKU. Count</span><span class="sxs-lookup"><span data-stu-id="fb9a6-103">EKUs.Count property</span></span>

<span data-ttu-id="fb9a6-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb9a6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fb9a6-105">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fb9a6-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fb9a6-106">La proprietà **count** Recupera il numero di oggetti [**EKU**](eku.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="fb9a6-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="fb9a6-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb9a6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9a6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb9a6-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="fb9a6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb9a6-109">Property value</span></span>

<span data-ttu-id="fb9a6-110">Numero di oggetti [**EKU**](eku.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="fb9a6-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="fb9a6-111">Ogni oggetto **EKU** rappresenta una singola proprietà di utilizzo chiavi avanzato (EKU) di un certificato.</span><span class="sxs-lookup"><span data-stu-id="fb9a6-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb9a6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb9a6-112">Remarks</span></span>

<span data-ttu-id="fb9a6-113">La proprietà **count** può essere usata per specificare l'ultimo oggetto [**EKU**](eku.md) in una raccolta durante il recupero di un oggetto **EKU** specifico usando la proprietà [**EKU. Item**](ekus-item.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9a6-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9a6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb9a6-114">Requirements</span></span>



| <span data-ttu-id="fb9a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb9a6-115">Requirement</span></span> | <span data-ttu-id="fb9a6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fb9a6-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9a6-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb9a6-117">End of client support</span></span><br/> | <span data-ttu-id="fb9a6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb9a6-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fb9a6-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fb9a6-119">End of server support</span></span><br/> | <span data-ttu-id="fb9a6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb9a6-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fb9a6-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fb9a6-121">Redistributable</span></span><br/>       | <span data-ttu-id="fb9a6-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb9a6-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fb9a6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fb9a6-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fb9a6-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb9a6-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
