---
description: Compila una catena di verifica del certificato per un certificato e restituisce un oggetto CertificateStatus che contiene lo stato di validità del certificato.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'Metodo ICertificate2:: IsValid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325022"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="69952-103">Metodo ICertificate2:: IsValid</span><span class="sxs-lookup"><span data-stu-id="69952-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="69952-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="69952-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="69952-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="69952-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="69952-106">Il metodo **IsValid** compila una catena di verifica del certificato per un certificato e restituisce un oggetto [**CertificateStatus**](certificatestatus.md) che contiene lo stato di validità del certificato.</span><span class="sxs-lookup"><span data-stu-id="69952-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="69952-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69952-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="69952-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="69952-108">Parameters</span></span>

<span data-ttu-id="69952-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="69952-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="69952-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69952-110">Requirements</span></span>



| <span data-ttu-id="69952-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="69952-111">Requirement</span></span> | <span data-ttu-id="69952-112">Valore</span><span class="sxs-lookup"><span data-stu-id="69952-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69952-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="69952-113">End of client support</span></span><br/> | <span data-ttu-id="69952-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69952-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="69952-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="69952-115">End of server support</span></span><br/> | <span data-ttu-id="69952-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69952-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="69952-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="69952-117">Redistributable</span></span><br/>       | <span data-ttu-id="69952-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="69952-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="69952-119">DLL</span><span class="sxs-lookup"><span data-stu-id="69952-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="69952-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69952-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69952-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69952-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69952-122">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="69952-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="69952-123">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="69952-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
