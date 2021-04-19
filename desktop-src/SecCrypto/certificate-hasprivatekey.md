---
description: Determina se al certificato è associata una chiave privata. Il metodo determina questa operazione controllando se \_ \_ è presente la proprietà CERT Key prova \_ info \_ prop \_ ID.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'Metodo ICertificate2:: HasPrivateKey'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324911"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="f6849-104">Metodo ICertificate2:: HasPrivateKey</span><span class="sxs-lookup"><span data-stu-id="f6849-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="f6849-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f6849-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f6849-106">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f6849-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f6849-107">Il metodo **HasPrivateKey** determina se al [*certificato*](../secgloss/c-gly.md) è associata una [*chiave privata*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f6849-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="f6849-108">Il metodo determina questa operazione controllando se \_ \_ è presente la proprietà CERT Key prova \_ info \_ prop \_ ID.</span><span class="sxs-lookup"><span data-stu-id="f6849-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6849-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6849-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="f6849-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6849-110">Parameters</span></span>

<span data-ttu-id="f6849-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f6849-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6849-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6849-112">Requirements</span></span>



| <span data-ttu-id="f6849-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6849-113">Requirement</span></span> | <span data-ttu-id="f6849-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f6849-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6849-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f6849-115">End of client support</span></span><br/> | <span data-ttu-id="f6849-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6849-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f6849-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f6849-117">End of server support</span></span><br/> | <span data-ttu-id="f6849-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6849-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f6849-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f6849-119">Redistributable</span></span><br/>       | <span data-ttu-id="f6849-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="f6849-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f6849-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f6849-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f6849-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6849-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6849-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6849-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6849-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="f6849-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="f6849-125">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="f6849-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f6849-126">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="f6849-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
