---
description: Recupera un valore booleano che indica se il bit bit keycertsign è impostato.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Proprietà DataUsage. IsKeyCertSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323949"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="7747e-103">Proprietà DataUsage. IsKeyCertSignEnabled</span><span class="sxs-lookup"><span data-stu-id="7747e-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="7747e-104">\[La proprietà **IsKeyCertSignEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7747e-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7747e-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7747e-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7747e-106">La proprietà **IsKeyCertSignEnabled** recupera un valore booleano che indica se il bit bit keycertsign è impostato.</span><span class="sxs-lookup"><span data-stu-id="7747e-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="7747e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7747e-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7747e-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7747e-108">Property value</span></span>

<span data-ttu-id="7747e-109">Se **true**, viene impostato il bit bit keycertsign.</span><span class="sxs-lookup"><span data-stu-id="7747e-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7747e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7747e-110">Requirements</span></span>



| <span data-ttu-id="7747e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7747e-111">Requirement</span></span> | <span data-ttu-id="7747e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7747e-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7747e-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7747e-113">Redistributable</span></span><br/> | <span data-ttu-id="7747e-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7747e-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7747e-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7747e-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="7747e-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7747e-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7747e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7747e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7747e-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="7747e-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
