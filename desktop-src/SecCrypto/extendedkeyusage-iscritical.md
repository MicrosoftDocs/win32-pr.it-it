---
description: Restituisce un valore booleano che indica se l'estensione EKU è contrassegnata come critica.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Proprietà ExtendedKeyUsage. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326896"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="bb398-103">Proprietà ExtendedKeyUsage. Critical</span><span class="sxs-lookup"><span data-stu-id="bb398-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="bb398-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb398-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bb398-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bb398-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bb398-106">La proprietà **ipocrita** restituisce un valore booleano che indica se l'estensione EKU è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="bb398-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb398-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb398-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bb398-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb398-108">Property value</span></span>

<span data-ttu-id="bb398-109">Se **true**, l'estensione EKU è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="bb398-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb398-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb398-110">Requirements</span></span>



| <span data-ttu-id="bb398-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb398-111">Requirement</span></span> | <span data-ttu-id="bb398-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bb398-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb398-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb398-113">End of client support</span></span><br/> | <span data-ttu-id="bb398-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb398-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb398-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bb398-115">End of server support</span></span><br/> | <span data-ttu-id="bb398-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb398-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb398-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bb398-117">Redistributable</span></span><br/>       | <span data-ttu-id="bb398-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb398-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb398-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bb398-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bb398-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb398-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb398-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb398-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb398-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="bb398-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
