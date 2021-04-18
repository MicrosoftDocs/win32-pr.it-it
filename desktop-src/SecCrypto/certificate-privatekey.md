---
description: Imposta o recupera la chiave privata associata al certificato.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Proprietà Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333959"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="6ac3d-103">Proprietà Certificate. PrivateKey</span><span class="sxs-lookup"><span data-stu-id="6ac3d-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="6ac3d-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6ac3d-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6ac3d-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ac3d-106">La proprietà **PrivateKey** imposta o recupera la chiave privata associata al certificato.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="6ac3d-107">Questa proprietà è stata introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="6ac3d-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac3d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ac3d-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="6ac3d-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6ac3d-110">Property value</span></span>

<span data-ttu-id="6ac3d-111">Oggetto [**PrivateKey**](privatekey.md) che rappresenta la chiave privata associata al certificato.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac3d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ac3d-112">Remarks</span></span>

<span data-ttu-id="6ac3d-113">Se si imposta la proprietà **PrivateKey** su Nothing, viene rimossa l'associazione tra la chiave privata e il certificato, ma la chiave privata non viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="6ac3d-114">Per eliminare la chiave privata, chiamare il metodo [**PrivateKey. Delete**](privatekey-delete.md) , quindi impostare questa proprietà su Nothing.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="6ac3d-115">Questa proprietà genera CAPICOM \_ E \_ non \_ è consentita quando viene impostata da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="6ac3d-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac3d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ac3d-116">Requirements</span></span>



| <span data-ttu-id="6ac3d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac3d-117">Requirement</span></span> | <span data-ttu-id="6ac3d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6ac3d-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac3d-119">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6ac3d-119">End of client support</span></span><br/> | <span data-ttu-id="6ac3d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ac3d-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ac3d-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6ac3d-121">End of server support</span></span><br/> | <span data-ttu-id="6ac3d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ac3d-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ac3d-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6ac3d-123">Redistributable</span></span><br/>       | <span data-ttu-id="6ac3d-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ac3d-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ac3d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6ac3d-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6ac3d-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ac3d-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac3d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ac3d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac3d-128">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="6ac3d-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
