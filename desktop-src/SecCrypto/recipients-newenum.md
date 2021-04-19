---
description: La \_ proprietà NewEnum dei destinatari recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Proprietà Recipients._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326350"
---
# <a name="recipients_newenum-property"></a><span data-ttu-id="9ae8f-104">Destinatari. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="9ae8f-104">Recipients.\_NewEnum property</span></span>

<span data-ttu-id="9ae8f-105">\[La proprietà **\_ NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9ae8f-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9ae8f-106">Usare invece la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="9ae8f-106">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9ae8f-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="9ae8f-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="9ae8f-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="9ae8f-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae8f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ae8f-109">Syntax</span></span>


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="9ae8f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9ae8f-110">Property value</span></span>

<span data-ttu-id="9ae8f-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="9ae8f-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ae8f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ae8f-112">Remarks</span></span>

<span data-ttu-id="9ae8f-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="9ae8f-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae8f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ae8f-114">Requirements</span></span>



| <span data-ttu-id="9ae8f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae8f-115">Requirement</span></span> | <span data-ttu-id="9ae8f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9ae8f-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae8f-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9ae8f-117">Redistributable</span></span><br/> | <span data-ttu-id="9ae8f-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ae8f-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9ae8f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae8f-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="9ae8f-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae8f-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae8f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ae8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae8f-122">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="9ae8f-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
