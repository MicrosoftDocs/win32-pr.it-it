---
description: Recupera un valore booleano che indica se il bit decipherOnly è impostato.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: Proprietà DataUsage. IsDecipherOnlyEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5ca72348220d6943ad367e88f404e0f3163f4c42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323962"
---
# <a name="keyusageisdecipheronlyenabled-property"></a><span data-ttu-id="50917-103">Proprietà DataUsage. IsDecipherOnlyEnabled</span><span class="sxs-lookup"><span data-stu-id="50917-103">KeyUsage.IsDecipherOnlyEnabled property</span></span>

<span data-ttu-id="50917-104">\[La proprietà **IsDecipherOnlyEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="50917-104">\[The **IsDecipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="50917-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="50917-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="50917-106">La proprietà **IsDecipherOnlyEnabled** recupera un valore booleano che indica se il bit decipherOnly è impostato.</span><span class="sxs-lookup"><span data-stu-id="50917-106">The **IsDecipherOnlyEnabled** property retrieves a Boolean value that indicates whether the decipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="50917-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50917-107">Syntax</span></span>


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="50917-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="50917-108">Property value</span></span>

<span data-ttu-id="50917-109">Se **true**, viene impostato il bit decipherOnly.</span><span class="sxs-lookup"><span data-stu-id="50917-109">If **true**, the decipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="50917-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50917-110">Requirements</span></span>



| <span data-ttu-id="50917-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="50917-111">Requirement</span></span> | <span data-ttu-id="50917-112">Valore</span><span class="sxs-lookup"><span data-stu-id="50917-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50917-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="50917-113">Redistributable</span></span><br/> | <span data-ttu-id="50917-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="50917-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="50917-115">DLL</span><span class="sxs-lookup"><span data-stu-id="50917-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="50917-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50917-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50917-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50917-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50917-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="50917-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
