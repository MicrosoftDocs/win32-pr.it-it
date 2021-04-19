---
description: Recupera un oggetto certificato che rappresenta il certificato indicizzato della raccolta. Si tratta della proprietà predefinita.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Proprietà Certificates. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332839"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="8d896-104">Proprietà Certificates. Item</span><span class="sxs-lookup"><span data-stu-id="8d896-104">Certificates.Item property</span></span>

<span data-ttu-id="8d896-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8d896-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8d896-106">Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8d896-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8d896-107">La proprietà **Item** recupera un oggetto [**certificato**](certificate.md) che rappresenta il certificato indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8d896-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="8d896-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="8d896-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d896-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d896-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="8d896-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8d896-110">Property value</span></span>

<span data-ttu-id="8d896-111">Oggetto [**certificato**](certificate.md) che rappresenta il certificato indicizzato.</span><span class="sxs-lookup"><span data-stu-id="8d896-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d896-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d896-112">Requirements</span></span>



| <span data-ttu-id="8d896-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d896-113">Requirement</span></span> | <span data-ttu-id="8d896-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8d896-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d896-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8d896-115">End of client support</span></span><br/> | <span data-ttu-id="8d896-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d896-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8d896-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8d896-117">End of server support</span></span><br/> | <span data-ttu-id="8d896-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d896-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8d896-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8d896-119">Redistributable</span></span><br/>       | <span data-ttu-id="8d896-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d896-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d896-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8d896-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8d896-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d896-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d896-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d896-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d896-124">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="8d896-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
