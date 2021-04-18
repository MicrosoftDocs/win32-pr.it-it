---
description: La \_ proprietà NewEnum degli attributi recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Proprietà Attributes._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329101"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="842d9-104">Attributi. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="842d9-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="842d9-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="842d9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="842d9-106">Usare invece la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="842d9-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="842d9-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="842d9-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="842d9-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="842d9-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="842d9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="842d9-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="842d9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="842d9-110">Property value</span></span>

<span data-ttu-id="842d9-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="842d9-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="842d9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="842d9-112">Remarks</span></span>

<span data-ttu-id="842d9-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="842d9-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="842d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842d9-114">Requirements</span></span>



| <span data-ttu-id="842d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="842d9-115">Requirement</span></span> | <span data-ttu-id="842d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="842d9-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="842d9-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="842d9-117">End of client support</span></span><br/> | <span data-ttu-id="842d9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="842d9-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="842d9-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="842d9-119">End of server support</span></span><br/> | <span data-ttu-id="842d9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="842d9-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="842d9-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="842d9-121">Redistributable</span></span><br/>       | <span data-ttu-id="842d9-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="842d9-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="842d9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="842d9-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="842d9-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="842d9-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842d9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="842d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842d9-126">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="842d9-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
