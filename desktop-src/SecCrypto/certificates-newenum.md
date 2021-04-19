---
description: La \_ proprietà NewEnum dei certificati recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Proprietà Certificates._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332926"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="2fcae-104">Certificati. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="2fcae-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="2fcae-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2fcae-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2fcae-106">Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2fcae-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2fcae-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fcae-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="2fcae-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2fcae-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcae-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fcae-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="2fcae-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2fcae-110">Property value</span></span>

<span data-ttu-id="2fcae-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="2fcae-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcae-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fcae-112">Remarks</span></span>

<span data-ttu-id="2fcae-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2fcae-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fcae-114">Requirements</span></span>



| <span data-ttu-id="2fcae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcae-115">Requirement</span></span> | <span data-ttu-id="2fcae-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcae-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcae-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2fcae-117">End of client support</span></span><br/> | <span data-ttu-id="2fcae-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fcae-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2fcae-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2fcae-119">End of server support</span></span><br/> | <span data-ttu-id="2fcae-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fcae-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2fcae-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2fcae-121">Redistributable</span></span><br/>       | <span data-ttu-id="2fcae-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2fcae-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2fcae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcae-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2fcae-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcae-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fcae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fcae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcae-126">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="2fcae-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
