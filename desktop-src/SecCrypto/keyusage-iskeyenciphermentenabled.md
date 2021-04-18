---
description: Recupera un valore booleano che indica se il bit keyEncipherment è impostato.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Proprietà DataUsage. IsKeyEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323948"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="d99ce-103">Proprietà DataUsage. IsKeyEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="d99ce-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="d99ce-104">\[La proprietà **IsKeyEnciphermentEnabled** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d99ce-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d99ce-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d99ce-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d99ce-106">La proprietà **IsKeyEnciphermentEnabled** recupera un valore booleano che indica se il bit keyEncipherment è impostato.</span><span class="sxs-lookup"><span data-stu-id="d99ce-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d99ce-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d99ce-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d99ce-108">Property value</span></span>

<span data-ttu-id="d99ce-109">Se **true**, viene impostato il bit keyEncipherment.</span><span class="sxs-lookup"><span data-stu-id="d99ce-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99ce-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d99ce-110">Requirements</span></span>



| <span data-ttu-id="d99ce-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d99ce-111">Requirement</span></span> | <span data-ttu-id="d99ce-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d99ce-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d99ce-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d99ce-113">Redistributable</span></span><br/> | <span data-ttu-id="d99ce-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d99ce-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d99ce-115">DLL</span><span class="sxs-lookup"><span data-stu-id="d99ce-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="d99ce-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d99ce-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99ce-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d99ce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99ce-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="d99ce-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
