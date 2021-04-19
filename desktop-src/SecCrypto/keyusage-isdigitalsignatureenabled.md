---
description: Recupera un valore booleano che indica se il bit digitalSignature è impostato.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: Proprietà DataUsage. IsDigitalSignatureEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323961"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="108e0-103">Proprietà DataUsage. IsDigitalSignatureEnabled</span><span class="sxs-lookup"><span data-stu-id="108e0-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="108e0-104">\[La proprietà **IsDigitalSignatureEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="108e0-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="108e0-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="108e0-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="108e0-106">La proprietà **IsDigitalSignatureEnabled** recupera un valore booleano che indica se il bit DigitalSignature è impostato.</span><span class="sxs-lookup"><span data-stu-id="108e0-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="108e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="108e0-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="108e0-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="108e0-108">Property value</span></span>

<span data-ttu-id="108e0-109">Se **true**, viene impostato il bit DigitalSignature.</span><span class="sxs-lookup"><span data-stu-id="108e0-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="108e0-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="108e0-110">Requirements</span></span>



| <span data-ttu-id="108e0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="108e0-111">Requirement</span></span> | <span data-ttu-id="108e0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="108e0-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="108e0-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="108e0-113">Redistributable</span></span><br/> | <span data-ttu-id="108e0-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="108e0-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="108e0-115">DLL</span><span class="sxs-lookup"><span data-stu-id="108e0-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="108e0-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="108e0-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="108e0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="108e0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108e0-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="108e0-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
