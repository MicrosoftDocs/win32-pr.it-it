---
description: Recupera il numero di oggetti qualificatore nella raccolta.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Proprietà Qualifiers. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333151"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="bd17e-103">Proprietà Qualifiers. Count</span><span class="sxs-lookup"><span data-stu-id="bd17e-103">Qualifiers.Count property</span></span>

<span data-ttu-id="bd17e-104">\[La proprietà **count** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bd17e-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bd17e-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="bd17e-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="bd17e-106">La proprietà **count** Recupera il numero di oggetti [**Qualifier**](qualifier.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd17e-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd17e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd17e-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="bd17e-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bd17e-108">Property value</span></span>

<span data-ttu-id="bd17e-109">Numero di oggetti [**qualificatori**](qualifier.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bd17e-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd17e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd17e-110">Requirements</span></span>



| <span data-ttu-id="bd17e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd17e-111">Requirement</span></span> | <span data-ttu-id="bd17e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bd17e-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd17e-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bd17e-113">Redistributable</span></span><br/> | <span data-ttu-id="bd17e-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd17e-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bd17e-115">DLL</span><span class="sxs-lookup"><span data-stu-id="bd17e-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bd17e-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd17e-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd17e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd17e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd17e-118">**Qualificatori**</span><span class="sxs-lookup"><span data-stu-id="bd17e-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
