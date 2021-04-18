---
description: Recupera il nome dell'archivio certificati rappresentato da questo oggetto.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Proprietà Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333870"
---
# <a name="storename-property"></a><span data-ttu-id="e04ce-103">Proprietà Store.Name</span><span class="sxs-lookup"><span data-stu-id="e04ce-103">Store.Name property</span></span>

<span data-ttu-id="e04ce-104">\[La proprietà [**Name**](store-location.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e04ce-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e04ce-105">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e04ce-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e04ce-106">La proprietà [**Name**](store-location.md) Recupera il nome dell'archivio certificati rappresentato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e04ce-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e04ce-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="e04ce-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e04ce-108">Property value</span></span>

<span data-ttu-id="e04ce-109">Valore **stringa** che rappresenta il nome dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="e04ce-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04ce-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e04ce-110">Remarks</span></span>

<span data-ttu-id="e04ce-111">Esempi di nomi di archivio certificati includono My e root.</span><span class="sxs-lookup"><span data-stu-id="e04ce-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="e04ce-112">Il valore della proprietà [**Name**](store-location.md) corrisponde al valore fornito per il parametro *StoreName* del metodo [**Open**](store-open.md) quando l'archivio è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="e04ce-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="e04ce-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e04ce-113">Requirements</span></span>



| <span data-ttu-id="e04ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e04ce-114">Requirement</span></span> | <span data-ttu-id="e04ce-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e04ce-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e04ce-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e04ce-116">Redistributable</span></span><br/> | <span data-ttu-id="e04ce-117">CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e04ce-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e04ce-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e04ce-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="e04ce-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e04ce-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04ce-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e04ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04ce-121">**Store**</span><span class="sxs-lookup"><span data-stu-id="e04ce-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
