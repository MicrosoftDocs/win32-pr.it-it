---
description: Recupera un oggetto OID dalla raccolta. Si tratta della proprietà predefinita.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: Proprietà Oid. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325159"
---
# <a name="oidsitem-property"></a><span data-ttu-id="b7c7c-104">Proprietà Oid. Item</span><span class="sxs-lookup"><span data-stu-id="b7c7c-104">OIDs.Item property</span></span>

<span data-ttu-id="b7c7c-105">\[La proprietà **Item** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b7c7c-105">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b7c7c-106">Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b7c7c-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b7c7c-107">La proprietà **Item** recupera un oggetto [**OID**](oid.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7c7c-107">The **Item** property retrieves an [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="b7c7c-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="b7c7c-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c7c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7c7c-109">Syntax</span></span>


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="b7c7c-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b7c7c-110">Property value</span></span>

<span data-ttu-id="b7c7c-111">Oggetto [**OID**](oid.md) in corrispondenza dell'indice specificato o dell'oggetto **OID** con il valore tratteggiato specificato.</span><span class="sxs-lookup"><span data-stu-id="b7c7c-111">The [**OID**](oid.md) object at the specified index, or the **OID** object with the specified dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c7c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7c7c-112">Requirements</span></span>



| <span data-ttu-id="b7c7c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c7c-113">Requirement</span></span> | <span data-ttu-id="b7c7c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b7c7c-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c7c-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b7c7c-115">Redistributable</span></span><br/> | <span data-ttu-id="b7c7c-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7c7c-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7c7c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="b7c7c-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="b7c7c-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7c7c-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c7c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7c7c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c7c-120">**OID**</span><span class="sxs-lookup"><span data-stu-id="b7c7c-120">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
