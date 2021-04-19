---
description: Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Proprietà Store. location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333152"
---
# <a name="storelocation-property"></a><span data-ttu-id="77567-103">Proprietà Store. location</span><span class="sxs-lookup"><span data-stu-id="77567-103">Store.Location property</span></span>

<span data-ttu-id="77567-104">\[La proprietà **location** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="77567-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="77567-105">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="77567-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="77567-106">La proprietà **location** Recupera il percorso dell'archivio certificati rappresentato da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="77567-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="77567-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77567-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="77567-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="77567-108">Property value</span></span>

<span data-ttu-id="77567-109">Il valore del [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) che rappresenta il percorso dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="77567-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="77567-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="77567-110">Remarks</span></span>

<span data-ttu-id="77567-111">Il valore della proprietà **location** corrisponde al valore fornito per il parametro *StoreLocation* del metodo [**Open**](store-open.md) quando l'archivio è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="77567-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="77567-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77567-112">Requirements</span></span>



| <span data-ttu-id="77567-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="77567-113">Requirement</span></span> | <span data-ttu-id="77567-114">Valore</span><span class="sxs-lookup"><span data-stu-id="77567-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77567-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="77567-115">Redistributable</span></span><br/> | <span data-ttu-id="77567-116">CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="77567-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="77567-117">DLL</span><span class="sxs-lookup"><span data-stu-id="77567-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="77567-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77567-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77567-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77567-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77567-120">**Store**</span><span class="sxs-lookup"><span data-stu-id="77567-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
