---
description: Recupera una raccolta dei qualificatori del criterio.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Proprietà PolicyInformation. Qualifiers (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324841"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="bb1cc-103">PolicyInformation. Qualifiers (proprietà)</span><span class="sxs-lookup"><span data-stu-id="bb1cc-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="bb1cc-104">\[La proprietà **qualificatori** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bb1cc-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb1cc-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per elaborare le informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="bb1cc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="bb1cc-106">La proprietà **Qualifiers** recupera una raccolta dei qualificatori del criterio.</span><span class="sxs-lookup"><span data-stu-id="bb1cc-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1cc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb1cc-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="bb1cc-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb1cc-108">Property value</span></span>

<span data-ttu-id="bb1cc-109">Il puntatore CPS (Certification Practice Statement) del criterio o i qualificatori delle notifiche utente come oggetto [**qualificatori**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1cc-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1cc-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb1cc-110">Requirements</span></span>



| <span data-ttu-id="bb1cc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb1cc-111">Requirement</span></span> | <span data-ttu-id="bb1cc-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bb1cc-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1cc-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bb1cc-113">Redistributable</span></span><br/> | <span data-ttu-id="bb1cc-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb1cc-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb1cc-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb1cc-115">Header</span></span><br/>          | <dl> <span data-ttu-id="bb1cc-116"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb1cc-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb1cc-117">DLL</span><span class="sxs-lookup"><span data-stu-id="bb1cc-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="bb1cc-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb1cc-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb1cc-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb1cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1cc-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="bb1cc-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
