---
description: Recupera un qualificatore in base a un indice specificato.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Proprietà Qualifiers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331270"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="3e262-103">Proprietà Qualifiers. Item</span><span class="sxs-lookup"><span data-stu-id="3e262-103">Qualifiers.Item property</span></span>

<span data-ttu-id="3e262-104">\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3e262-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e262-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="3e262-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="3e262-106">La proprietà **Item** recupera un qualificatore in base a un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3e262-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="3e262-107">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="3e262-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e262-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e262-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="3e262-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3e262-109">Property value</span></span>

<span data-ttu-id="3e262-110">Oggetto [**qualificatore**](qualifier.md) che rappresenta il qualificatore indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="3e262-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e262-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e262-111">Requirements</span></span>



| <span data-ttu-id="3e262-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e262-112">Requirement</span></span> | <span data-ttu-id="3e262-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3e262-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e262-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3e262-114">Redistributable</span></span><br/> | <span data-ttu-id="3e262-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e262-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3e262-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3e262-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="3e262-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e262-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e262-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e262-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e262-119">**Qualificatori**</span><span class="sxs-lookup"><span data-stu-id="3e262-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
