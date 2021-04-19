---
description: Recupera un valore booleano che indica se il bit dataEncipherment è impostato.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Proprietà DataUsage. IsDataEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323963"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="9076f-103">Proprietà DataUsage. IsDataEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="9076f-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="9076f-104">\[La proprietà **IsDataEnciphermentEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9076f-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9076f-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9076f-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9076f-106">La proprietà **IsDataEnciphermentEnabled** recupera un valore booleano che indica se il bit dataEncipherment è impostato.</span><span class="sxs-lookup"><span data-stu-id="9076f-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="9076f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9076f-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9076f-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9076f-108">Property value</span></span>

<span data-ttu-id="9076f-109">Se **true**, viene impostato il bit dataEncipherment.</span><span class="sxs-lookup"><span data-stu-id="9076f-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9076f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9076f-110">Requirements</span></span>



| <span data-ttu-id="9076f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9076f-111">Requirement</span></span> | <span data-ttu-id="9076f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9076f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9076f-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9076f-113">Redistributable</span></span><br/> | <span data-ttu-id="9076f-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9076f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9076f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="9076f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="9076f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9076f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9076f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9076f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9076f-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="9076f-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
