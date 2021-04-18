---
description: La \_ proprietà NewEnum di EKU recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: c7d038c0-416f-47f7-94ba-74ca877da7ba
title: Proprietà EKUs._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 72605e0ad7bbb8671ff9a5885a79f1d7836c6efb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324240"
---
# <a name="ekus_newenum-property"></a><span data-ttu-id="6f2de-104">EKU. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="6f2de-104">EKUs.\_NewEnum property</span></span>

<span data-ttu-id="6f2de-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f2de-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6f2de-106">Usare invece la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6f2de-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6f2de-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f2de-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="6f2de-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6f2de-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f2de-109">Syntax</span></span>


```VB
EKUs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="6f2de-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6f2de-110">Property value</span></span>

<span data-ttu-id="6f2de-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f2de-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f2de-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f2de-112">Remarks</span></span>

<span data-ttu-id="6f2de-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6f2de-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f2de-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f2de-114">Requirements</span></span>



| <span data-ttu-id="6f2de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f2de-115">Requirement</span></span> | <span data-ttu-id="6f2de-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6f2de-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2de-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6f2de-117">End of client support</span></span><br/> | <span data-ttu-id="6f2de-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f2de-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6f2de-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6f2de-119">End of server support</span></span><br/> | <span data-ttu-id="6f2de-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f2de-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6f2de-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6f2de-121">Redistributable</span></span><br/>       | <span data-ttu-id="6f2de-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f2de-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6f2de-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6f2de-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6f2de-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f2de-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f2de-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f2de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2de-126">**EKU**</span><span class="sxs-lookup"><span data-stu-id="6f2de-126">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
