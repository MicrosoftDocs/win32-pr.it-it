---
description: La proprietà Item recupera un'estensione, in base all'indice, dalla raccolta. Si tratta della proprietà predefinita.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Proprietà Extensions. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326515"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="b8e75-104">Proprietà Extensions. Item</span><span class="sxs-lookup"><span data-stu-id="b8e75-104">Extensions.Item property</span></span>

<span data-ttu-id="b8e75-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8e75-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b8e75-106">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b8e75-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b8e75-107">La proprietà **Item** recupera un'estensione, in base all'indice, dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="b8e75-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="b8e75-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="b8e75-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e75-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8e75-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="b8e75-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b8e75-110">Property value</span></span>

<span data-ttu-id="b8e75-111">Oggetto di [**estensione**](extension.md) che rappresenta l'estensione del certificato indicizzato della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b8e75-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e75-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8e75-112">Requirements</span></span>



| <span data-ttu-id="b8e75-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e75-113">Requirement</span></span> | <span data-ttu-id="b8e75-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e75-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e75-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b8e75-115">End of client support</span></span><br/> | <span data-ttu-id="b8e75-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8e75-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b8e75-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b8e75-117">End of server support</span></span><br/> | <span data-ttu-id="b8e75-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8e75-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b8e75-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b8e75-119">Redistributable</span></span><br/>       | <span data-ttu-id="b8e75-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8e75-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b8e75-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e75-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b8e75-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e75-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e75-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e75-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e75-124">**Estensioni**</span><span class="sxs-lookup"><span data-stu-id="b8e75-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
