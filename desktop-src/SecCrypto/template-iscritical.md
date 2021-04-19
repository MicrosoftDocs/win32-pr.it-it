---
description: Recupera un valore booleano che indica se l'estensione del modello è contrassegnata come critica.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Proprietà Template. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328429"
---
# <a name="templateiscritical-property"></a><span data-ttu-id="6f8ef-103">Proprietà Template. Critical</span><span class="sxs-lookup"><span data-stu-id="6f8ef-103">Template.IsCritical property</span></span>

<span data-ttu-id="6f8ef-104">\[La proprietà **ipocrita** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6f8ef-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="6f8ef-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="6f8ef-106">La proprietà **ipocrita** recupera un valore booleano che indica se l'estensione del modello è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-106">The **IsCritical** property retrieves a Boolean value that indicates whether the template extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8ef-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f8ef-107">Syntax</span></span>


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6f8ef-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6f8ef-108">Property value</span></span>

<span data-ttu-id="6f8ef-109">Se **true**, l'estensione del modello è contrassegnata come critica.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-109">If **true**, the template extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f8ef-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f8ef-110">Requirements</span></span>



| <span data-ttu-id="6f8ef-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f8ef-111">Requirement</span></span> | <span data-ttu-id="6f8ef-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6f8ef-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8ef-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6f8ef-113">Redistributable</span></span><br/> | <span data-ttu-id="6f8ef-114">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f8ef-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6f8ef-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8ef-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6f8ef-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f8ef-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f8ef-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f8ef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f8ef-118">**Modello**</span><span class="sxs-lookup"><span data-stu-id="6f8ef-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
