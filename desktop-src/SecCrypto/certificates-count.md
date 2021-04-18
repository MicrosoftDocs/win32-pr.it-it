---
description: Recupera il numero di oggetti certificato nell'insieme.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Proprietà Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328315"
---
# <a name="certificatescount-property"></a><span data-ttu-id="6be66-103">Proprietà Certificates. Count</span><span class="sxs-lookup"><span data-stu-id="6be66-103">Certificates.Count property</span></span>

<span data-ttu-id="6be66-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6be66-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6be66-105">Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6be66-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6be66-106">La proprietà **count** Recupera il numero di oggetti [**certificato**](certificate.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6be66-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be66-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6be66-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="6be66-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6be66-108">Property value</span></span>

<span data-ttu-id="6be66-109">Numero di oggetti [**certificato**](certificate.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6be66-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="6be66-110">Ogni oggetto **certificato** rappresenta un singolo certificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6be66-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be66-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6be66-111">Remarks</span></span>

<span data-ttu-id="6be66-112">CAPICOM supporta solo un certificato singolo per l'archivio delle [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6be66-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="6be66-113">Anche se l'archivio delle smart card contiene più di un certificato, questa proprietà conterrà 1.</span><span class="sxs-lookup"><span data-stu-id="6be66-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="6be66-114">Per ulteriori informazioni sull'archivio delle smart card, vedere il membro dell' **\_ Archivio dell' \_ \_ utente \_ della smart card CAPICOM** dell'enumerazione del [**\_ \_ percorso dell'archivio CAPICOM**](capicom-store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="6be66-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be66-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6be66-115">Requirements</span></span>



| <span data-ttu-id="6be66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be66-116">Requirement</span></span> | <span data-ttu-id="6be66-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6be66-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6be66-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6be66-118">End of client support</span></span><br/> | <span data-ttu-id="6be66-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6be66-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6be66-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6be66-120">End of server support</span></span><br/> | <span data-ttu-id="6be66-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6be66-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6be66-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6be66-122">Redistributable</span></span><br/>       | <span data-ttu-id="6be66-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6be66-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6be66-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6be66-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6be66-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6be66-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be66-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6be66-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be66-127">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="6be66-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
