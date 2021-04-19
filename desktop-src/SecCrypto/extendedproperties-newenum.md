---
description: La \_ proprietà NewEnum di ExtendedProperties recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: Proprietà ExtendedProperties._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328741"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="437d6-104">ExtendedProperty. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="437d6-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="437d6-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="437d6-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="437d6-106">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="437d6-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="437d6-107">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="437d6-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="437d6-108">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="437d6-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="437d6-109">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="437d6-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="437d6-110">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="437d6-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="437d6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="437d6-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="437d6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="437d6-112">Property value</span></span>

<span data-ttu-id="437d6-113">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="437d6-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="437d6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="437d6-114">Remarks</span></span>

<span data-ttu-id="437d6-115">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="437d6-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="437d6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="437d6-116">Requirements</span></span>



| <span data-ttu-id="437d6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="437d6-117">Requirement</span></span> | <span data-ttu-id="437d6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="437d6-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="437d6-119">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="437d6-119">End of client support</span></span><br/> | <span data-ttu-id="437d6-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="437d6-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="437d6-121">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="437d6-121">End of server support</span></span><br/> | <span data-ttu-id="437d6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="437d6-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="437d6-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="437d6-123">Redistributable</span></span><br/>       | <span data-ttu-id="437d6-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="437d6-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="437d6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="437d6-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="437d6-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="437d6-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
