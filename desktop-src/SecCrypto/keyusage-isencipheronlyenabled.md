---
description: Recupera un valore booleano che indica se il bit encipherOnly è impostato.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: Proprietà DataUsage. IsEncipherOnlyEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323960"
---
# <a name="keyusageisencipheronlyenabled-property"></a><span data-ttu-id="0ca06-103">Proprietà DataUsage. IsEncipherOnlyEnabled</span><span class="sxs-lookup"><span data-stu-id="0ca06-103">KeyUsage.IsEncipherOnlyEnabled property</span></span>

<span data-ttu-id="0ca06-104">\[La proprietà **IsEncipherOnlyEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0ca06-104">\[The **IsEncipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0ca06-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0ca06-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0ca06-106">La proprietà **IsEncipherOnlyEnabled** recupera un valore booleano che indica se il bit encipherOnly è impostato.</span><span class="sxs-lookup"><span data-stu-id="0ca06-106">The **IsEncipherOnlyEnabled** property retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca06-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ca06-107">Syntax</span></span>


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0ca06-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0ca06-108">Property value</span></span>

<span data-ttu-id="0ca06-109">Se **true**, viene impostato il bit encipherOnly.</span><span class="sxs-lookup"><span data-stu-id="0ca06-109">If **true**, the encipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca06-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ca06-110">Requirements</span></span>



| <span data-ttu-id="0ca06-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca06-111">Requirement</span></span> | <span data-ttu-id="0ca06-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0ca06-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca06-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0ca06-113">Redistributable</span></span><br/> | <span data-ttu-id="0ca06-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ca06-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0ca06-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0ca06-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="0ca06-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ca06-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca06-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ca06-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca06-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="0ca06-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
