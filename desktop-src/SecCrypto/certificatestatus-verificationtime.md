---
description: Imposta o recupera l'ora in cui il certificato è stato verificato.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Proprietà CertificateStatus. VerificationTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324132"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="98baf-103">Proprietà CertificateStatus. VerificationTime</span><span class="sxs-lookup"><span data-stu-id="98baf-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="98baf-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98baf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="98baf-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="98baf-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="98baf-106">La proprietà **VerificationTime** imposta o recupera l'ora in cui il certificato è stato verificato.</span><span class="sxs-lookup"><span data-stu-id="98baf-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="98baf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98baf-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="98baf-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="98baf-108">Property value</span></span>

<span data-ttu-id="98baf-109">Ora di verifica del certificato.</span><span class="sxs-lookup"><span data-stu-id="98baf-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="98baf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="98baf-110">Remarks</span></span>

<span data-ttu-id="98baf-111">Se questa proprietà non è impostata, viene utilizzata l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="98baf-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="98baf-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98baf-112">Requirements</span></span>



| <span data-ttu-id="98baf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98baf-113">Requirement</span></span> | <span data-ttu-id="98baf-114">Valore</span><span class="sxs-lookup"><span data-stu-id="98baf-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98baf-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="98baf-115">End of client support</span></span><br/> | <span data-ttu-id="98baf-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98baf-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98baf-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="98baf-117">End of server support</span></span><br/> | <span data-ttu-id="98baf-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98baf-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98baf-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="98baf-119">Redistributable</span></span><br/>       | <span data-ttu-id="98baf-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="98baf-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98baf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="98baf-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="98baf-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98baf-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
