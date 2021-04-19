---
description: Recupera un valore booleano che indica se l'estensione per l'utilizzo dei dati è contrassegnata come critica.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: Proprietà di utilizzo chiave. ipocrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323965"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="431a8-103">Proprietà di utilizzo chiave. ipocrita</span><span class="sxs-lookup"><span data-stu-id="431a8-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="431a8-104">\[La proprietà **ipocrita** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="431a8-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="431a8-105">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="431a8-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="431a8-106">La proprietà **ipocrita** recupera un valore booleano che indica se l'estensione per l'utilizzo delle chiave è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="431a8-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="431a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="431a8-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="431a8-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="431a8-108">Property value</span></span>

<span data-ttu-id="431a8-109">Se **true**, l'estensione per l'utilizzo delle chiave è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="431a8-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="431a8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="431a8-110">Requirements</span></span>



| <span data-ttu-id="431a8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="431a8-111">Requirement</span></span> | <span data-ttu-id="431a8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="431a8-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="431a8-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="431a8-113">Redistributable</span></span><br/> | <span data-ttu-id="431a8-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="431a8-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="431a8-115">DLL</span><span class="sxs-lookup"><span data-stu-id="431a8-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="431a8-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431a8-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431a8-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="431a8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431a8-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="431a8-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
