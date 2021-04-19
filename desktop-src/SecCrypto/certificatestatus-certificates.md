---
description: Imposta o recupera la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Proprietà CertificateStatus. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326043"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="9cc48-103">Proprietà CertificateStatus. Certificates</span><span class="sxs-lookup"><span data-stu-id="9cc48-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="9cc48-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9cc48-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9cc48-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9cc48-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9cc48-106">La proprietà **Certificates** imposta o recupera la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="9cc48-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc48-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="9cc48-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9cc48-108">Property value</span></span>

<span data-ttu-id="9cc48-109">Oggetto [**Certificates**](certificates.md) che rappresenta la raccolta di certificati che possono essere utilizzati per compilare la catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="9cc48-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc48-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc48-110">Requirements</span></span>



| <span data-ttu-id="9cc48-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc48-111">Requirement</span></span> | <span data-ttu-id="9cc48-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc48-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc48-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9cc48-113">End of client support</span></span><br/> | <span data-ttu-id="9cc48-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cc48-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9cc48-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9cc48-115">End of server support</span></span><br/> | <span data-ttu-id="9cc48-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cc48-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9cc48-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9cc48-117">Redistributable</span></span><br/>       | <span data-ttu-id="9cc48-118">CAPICOM 2,1 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9cc48-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9cc48-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc48-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9cc48-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc48-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
