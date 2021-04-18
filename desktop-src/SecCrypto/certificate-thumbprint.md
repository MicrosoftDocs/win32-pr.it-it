---
description: Recupera una stringa esadecimale contenente l'hash SHA-1 del certificato.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Proprietà Certificate. identificazione personale
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324904"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="e3c82-103">Proprietà Certificate. identificazione personale</span><span class="sxs-lookup"><span data-stu-id="e3c82-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="e3c82-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3c82-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e3c82-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e3c82-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e3c82-106">La proprietà **identificazione personale** recupera una stringa esadecimale contenente l'hash [*SHA-1*](../secgloss/s-gly.md) del certificato.</span><span class="sxs-lookup"><span data-stu-id="e3c82-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="e3c82-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e3c82-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c82-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3c82-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="e3c82-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e3c82-109">Property value</span></span>

<span data-ttu-id="e3c82-110">Stringa esadecimale contenente l'hash SHA-1 del certificato.</span><span class="sxs-lookup"><span data-stu-id="e3c82-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c82-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3c82-111">Requirements</span></span>



| <span data-ttu-id="e3c82-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c82-112">Requirement</span></span> | <span data-ttu-id="e3c82-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e3c82-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c82-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e3c82-114">End of client support</span></span><br/> | <span data-ttu-id="e3c82-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3c82-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e3c82-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e3c82-116">End of server support</span></span><br/> | <span data-ttu-id="e3c82-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3c82-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e3c82-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e3c82-118">Redistributable</span></span><br/>       | <span data-ttu-id="e3c82-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e3c82-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e3c82-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e3c82-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e3c82-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3c82-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c82-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3c82-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c82-123">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="e3c82-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
