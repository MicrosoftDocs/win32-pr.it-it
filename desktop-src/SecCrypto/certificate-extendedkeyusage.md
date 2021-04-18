---
description: Restituisce un oggetto ExtendedKeyUsage che indica gli utilizzi validi del certificato.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'Metodo ICertificate2:: ExtendedKeyUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328007"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="d86a9-103">Metodo ICertificate2:: ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="d86a9-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="d86a9-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d86a9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d86a9-105">Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d86a9-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d86a9-106">Il metodo **ExtendedKeyUsage** restituisce un oggetto [**ExtendedKeyUsage**](extendedkeyusage.md) che indica gli utilizzi validi del certificato.</span><span class="sxs-lookup"><span data-stu-id="d86a9-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d86a9-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="d86a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d86a9-108">Parameters</span></span>

<span data-ttu-id="d86a9-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d86a9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d86a9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d86a9-110">Return value</span></span>

<span data-ttu-id="d86a9-111">Oggetto [**ExtendedKeyUsage**](extendedkeyusage.md) associato al certificato.</span><span class="sxs-lookup"><span data-stu-id="d86a9-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86a9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d86a9-112">Requirements</span></span>



| <span data-ttu-id="d86a9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86a9-113">Requirement</span></span> | <span data-ttu-id="d86a9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d86a9-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d86a9-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d86a9-115">End of client support</span></span><br/> | <span data-ttu-id="d86a9-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d86a9-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d86a9-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d86a9-117">End of server support</span></span><br/> | <span data-ttu-id="d86a9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d86a9-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d86a9-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d86a9-119">Redistributable</span></span><br/>       | <span data-ttu-id="d86a9-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d86a9-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d86a9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d86a9-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d86a9-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d86a9-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86a9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d86a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86a9-124">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="d86a9-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="d86a9-125">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="d86a9-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
