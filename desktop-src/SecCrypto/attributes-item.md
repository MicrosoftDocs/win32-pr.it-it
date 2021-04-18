---
description: Recupera l'oggetto attributo che rappresenta l'attributo indicizzato.
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Proprietà Attributes. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 208e36fd8d4d7e3effc2c0f59b7db921fed76d79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329103"
---
# <a name="attributesitem-property"></a><span data-ttu-id="ff172-103">Proprietà Attributes. Item</span><span class="sxs-lookup"><span data-stu-id="ff172-103">Attributes.Item property</span></span>

<span data-ttu-id="ff172-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff172-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="ff172-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="ff172-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ff172-106">La proprietà **Item** recupera l'oggetto [**attributo**](attribute.md) che rappresenta l'attributo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="ff172-106">The **Item** property retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="ff172-107">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="ff172-107">This is the default property.</span></span>

<span data-ttu-id="ff172-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ff172-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff172-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff172-109">Syntax</span></span>


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ff172-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ff172-110">Property value</span></span>

<span data-ttu-id="ff172-111">Oggetto [**attributo**](attribute.md) che rappresenta l'attributo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="ff172-111">An [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff172-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff172-112">Requirements</span></span>



| <span data-ttu-id="ff172-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff172-113">Requirement</span></span> | <span data-ttu-id="ff172-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ff172-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff172-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ff172-115">End of client support</span></span><br/> | <span data-ttu-id="ff172-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff172-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff172-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ff172-117">End of server support</span></span><br/> | <span data-ttu-id="ff172-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff172-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff172-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ff172-119">Redistributable</span></span><br/>       | <span data-ttu-id="ff172-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff172-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ff172-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ff172-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ff172-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff172-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
