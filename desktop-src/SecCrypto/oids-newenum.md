---
description: La \_ proprietà NewEnum di OID recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: Proprietà OIDs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325158"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="998a9-104">OID. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="998a9-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="998a9-105">\[La proprietà **\_ NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="998a9-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="998a9-106">Usare invece la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="998a9-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="998a9-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="998a9-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="998a9-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="998a9-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="998a9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="998a9-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="998a9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="998a9-110">Property value</span></span>

<span data-ttu-id="998a9-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="998a9-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="998a9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="998a9-112">Remarks</span></span>

<span data-ttu-id="998a9-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="998a9-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="998a9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="998a9-114">Requirements</span></span>



| <span data-ttu-id="998a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="998a9-115">Requirement</span></span> | <span data-ttu-id="998a9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="998a9-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="998a9-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="998a9-117">Redistributable</span></span><br/> | <span data-ttu-id="998a9-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="998a9-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="998a9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="998a9-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="998a9-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="998a9-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="998a9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="998a9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998a9-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="998a9-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
