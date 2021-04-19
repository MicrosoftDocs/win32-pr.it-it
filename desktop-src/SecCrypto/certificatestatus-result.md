---
description: La proprietà Result recupera un valore che indica se il certificato è valido. Si tratta della proprietà predefinita.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Proprietà CertificateStatus. Result
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324139"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="bcd00-104">Proprietà CertificateStatus. Result</span><span class="sxs-lookup"><span data-stu-id="bcd00-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="bcd00-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bcd00-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bcd00-106">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bcd00-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bcd00-107">La proprietà **result** recupera un valore che indica se il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="bcd00-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="bcd00-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="bcd00-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd00-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcd00-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bcd00-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bcd00-110">Property value</span></span>

<span data-ttu-id="bcd00-111">Se **true**, il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="bcd00-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="bcd00-112">La validità del certificato viene controllata usando l'impostazione corrente della proprietà [**CheckFlag**](certificatestatus-checkflag.md) e le diverse impostazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="bcd00-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd00-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcd00-113">Requirements</span></span>



| <span data-ttu-id="bcd00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd00-114">Requirement</span></span> | <span data-ttu-id="bcd00-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bcd00-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd00-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bcd00-116">End of client support</span></span><br/> | <span data-ttu-id="bcd00-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcd00-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bcd00-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bcd00-118">End of server support</span></span><br/> | <span data-ttu-id="bcd00-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcd00-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bcd00-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bcd00-120">Redistributable</span></span><br/>       | <span data-ttu-id="bcd00-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bcd00-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bcd00-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd00-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bcd00-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd00-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
