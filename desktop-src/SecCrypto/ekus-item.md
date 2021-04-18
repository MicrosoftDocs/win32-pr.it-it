---
description: Recupera l'oggetto EKU che rappresenta la proprietà di utilizzo chiavi avanzato (EKU) indicizzato.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Proprietà IEKUs:: Item'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330904"
---
# <a name="iekusitem-property"></a><span data-ttu-id="bf69a-103">Proprietà IEKUs:: Item</span><span class="sxs-lookup"><span data-stu-id="bf69a-103">IEKUs::Item property</span></span>

<span data-ttu-id="bf69a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf69a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bf69a-105">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bf69a-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bf69a-106">La proprietà **Item** recupera l'oggetto [**EKU**](eku.md) che rappresenta la proprietà di utilizzo chiavi avanzato (EKU) indicizzato.</span><span class="sxs-lookup"><span data-stu-id="bf69a-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="bf69a-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bf69a-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf69a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf69a-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="bf69a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bf69a-109">Property value</span></span>

<span data-ttu-id="bf69a-110">Oggetto [**EKU**](eku.md) che rappresenta la proprietà di utilizzo chiavi avanzato (EKU) indicizzato.</span><span class="sxs-lookup"><span data-stu-id="bf69a-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf69a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf69a-111">Requirements</span></span>



| <span data-ttu-id="bf69a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf69a-112">Requirement</span></span> | <span data-ttu-id="bf69a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="bf69a-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf69a-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bf69a-114">End of client support</span></span><br/> | <span data-ttu-id="bf69a-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf69a-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bf69a-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bf69a-116">End of server support</span></span><br/> | <span data-ttu-id="bf69a-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf69a-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bf69a-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bf69a-118">Redistributable</span></span><br/>       | <span data-ttu-id="bf69a-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf69a-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bf69a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bf69a-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bf69a-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf69a-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf69a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf69a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf69a-123">**EKU**</span><span class="sxs-lookup"><span data-stu-id="bf69a-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
