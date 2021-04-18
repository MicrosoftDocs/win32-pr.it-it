---
description: La \_ proprietà NewEnum dei qualificatori recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta. Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Proprietà Qualifiers._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326976"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="c2df9-104">Qualificatori. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="c2df9-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="c2df9-105">\[La proprietà **\_ NewEnum** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c2df9-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2df9-106">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="c2df9-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="c2df9-107">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c2df9-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c2df9-108">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c2df9-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2df9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2df9-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="c2df9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c2df9-110">Property value</span></span>

<span data-ttu-id="c2df9-111">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="c2df9-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2df9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2df9-112">Remarks</span></span>

<span data-ttu-id="c2df9-113">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c2df9-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2df9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2df9-114">Requirements</span></span>



| <span data-ttu-id="c2df9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2df9-115">Requirement</span></span> | <span data-ttu-id="c2df9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c2df9-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2df9-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c2df9-117">Redistributable</span></span><br/> | <span data-ttu-id="c2df9-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2df9-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c2df9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c2df9-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="c2df9-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2df9-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2df9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2df9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2df9-122">**Qualificatori**</span><span class="sxs-lookup"><span data-stu-id="c2df9-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
