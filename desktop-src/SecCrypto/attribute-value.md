---
description: Imposta o Recupera il valore dell'attributo.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Proprietà Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330754"
---
# <a name="attributevalue-property"></a><span data-ttu-id="4e5d2-103">Proprietà Attribute. Value</span><span class="sxs-lookup"><span data-stu-id="4e5d2-103">Attribute.Value property</span></span>

<span data-ttu-id="4e5d2-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4e5d2-105">Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="4e5d2-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4e5d2-106">La proprietà **value** imposta o Recupera il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="4e5d2-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e5d2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e5d2-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="4e5d2-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4e5d2-109">Property value</span></span>

<span data-ttu-id="4e5d2-110">Variabile **Variant** che contiene il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="4e5d2-111">Per gli attributi di tempo di firma dell'attributo con autenticazione di CAPICOM, il tipo di dati è **date**. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e5d2-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="4e5d2-112">Per tutti gli altri attributi, il valore della proprietà è una stringa.</span><span class="sxs-lookup"><span data-stu-id="4e5d2-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5d2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e5d2-113">Requirements</span></span>



| <span data-ttu-id="4e5d2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e5d2-114">Requirement</span></span> | <span data-ttu-id="4e5d2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4e5d2-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5d2-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4e5d2-116">End of client support</span></span><br/> | <span data-ttu-id="4e5d2-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e5d2-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4e5d2-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4e5d2-118">End of server support</span></span><br/> | <span data-ttu-id="4e5d2-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e5d2-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4e5d2-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4e5d2-120">Redistributable</span></span><br/>       | <span data-ttu-id="4e5d2-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e5d2-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4e5d2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4e5d2-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4e5d2-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e5d2-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
