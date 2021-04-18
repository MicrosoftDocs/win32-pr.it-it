---
description: La \_ proprietà NewEnum di CertificatePolicies recupera un'interfaccia IEnumVARIANT su un oggetto che può essere utilizzato per enumerare la raccolta.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: Proprietà CertificatePolicies._NewEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330028"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="78eca-103">CertificatePolicies. \_ Proprietà NewEnum</span><span class="sxs-lookup"><span data-stu-id="78eca-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="78eca-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78eca-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="78eca-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per i criteri di certificato per recuperare i criteri del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="78eca-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="78eca-106">La proprietà **\_ NewEnum** recupera un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="78eca-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="78eca-107">Questa proprietà è nascosta all'interno di Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="78eca-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="78eca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78eca-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="78eca-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78eca-109">Property value</span></span>

<span data-ttu-id="78eca-110">Interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) su un oggetto che può essere utilizzato per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="78eca-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="78eca-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="78eca-111">Remarks</span></span>

<span data-ttu-id="78eca-112">Questa proprietà viene automaticamente utilizzata internamente quando si utilizza il `For Each In` costrutto in Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="78eca-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="78eca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78eca-113">Requirements</span></span>



| <span data-ttu-id="78eca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="78eca-114">Requirement</span></span> | <span data-ttu-id="78eca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="78eca-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78eca-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78eca-116">End of client support</span></span><br/> | <span data-ttu-id="78eca-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78eca-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="78eca-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78eca-118">End of server support</span></span><br/> | <span data-ttu-id="78eca-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78eca-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="78eca-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="78eca-120">Redistributable</span></span><br/>       | <span data-ttu-id="78eca-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="78eca-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="78eca-122">DLL</span><span class="sxs-lookup"><span data-stu-id="78eca-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="78eca-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78eca-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
