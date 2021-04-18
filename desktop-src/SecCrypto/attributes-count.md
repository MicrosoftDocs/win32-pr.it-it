---
description: Recupera il numero di oggetti attributo nell'insieme.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Proprietà Attributes. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329104"
---
# <a name="attributescount-property"></a><span data-ttu-id="4c644-103">Proprietà Attributes. Count</span><span class="sxs-lookup"><span data-stu-id="4c644-103">Attributes.Count property</span></span>

<span data-ttu-id="4c644-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c644-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4c644-105">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="4c644-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4c644-106">La proprietà **count** Recupera il numero di oggetti [**attribute**](attribute.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="4c644-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="4c644-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4c644-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c644-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c644-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="4c644-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4c644-109">Property value</span></span>

<span data-ttu-id="4c644-110">Numero di oggetti [**attributo**](attribute.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="4c644-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="4c644-111">Ogni oggetto **attributo** rappresenta un singolo attributo nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="4c644-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c644-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c644-112">Remarks</span></span>

<span data-ttu-id="4c644-113">È possibile utilizzare la proprietà **count** per specificare l'ultimo oggetto [**attributo**](attribute.md) nella raccolta durante il recupero di un oggetto **attributo** specifico utilizzando la proprietà [**Attributes. Item**](attributes-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4c644-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c644-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c644-114">Requirements</span></span>



| <span data-ttu-id="4c644-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c644-115">Requirement</span></span> | <span data-ttu-id="4c644-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4c644-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c644-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4c644-117">End of client support</span></span><br/> | <span data-ttu-id="4c644-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c644-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c644-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4c644-119">End of server support</span></span><br/> | <span data-ttu-id="4c644-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c644-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c644-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4c644-121">Redistributable</span></span><br/>       | <span data-ttu-id="4c644-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c644-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4c644-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4c644-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4c644-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c644-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c644-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c644-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c644-126">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="4c644-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
