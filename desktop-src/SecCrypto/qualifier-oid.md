---
description: Recupera l'ID oggetto del qualificatore.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Proprietà Qualifier. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329011"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="7ed1c-103">Proprietà Qualifier. OID</span><span class="sxs-lookup"><span data-stu-id="7ed1c-103">Qualifier.OID property</span></span>

<span data-ttu-id="7ed1c-104">\[La proprietà **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7ed1c-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ed1c-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare l'OID per i criteri dei certificati per elaborare i qualificatori che fanno parte delle informazioni sui criteri nell'estensione criteri di certificato.\]</span><span class="sxs-lookup"><span data-stu-id="7ed1c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="7ed1c-106">La proprietà **OID** recupera l'ID oggetto del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="7ed1c-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="7ed1c-107">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ed1c-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ed1c-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="7ed1c-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7ed1c-109">Property value</span></span>

<span data-ttu-id="7ed1c-110">Oggetto [**OID**](oid.md) che identifica il qualificatore.</span><span class="sxs-lookup"><span data-stu-id="7ed1c-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed1c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ed1c-111">Requirements</span></span>



| <span data-ttu-id="7ed1c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed1c-112">Requirement</span></span> | <span data-ttu-id="7ed1c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7ed1c-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed1c-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7ed1c-114">Redistributable</span></span><br/> | <span data-ttu-id="7ed1c-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ed1c-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ed1c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7ed1c-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="7ed1c-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ed1c-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ed1c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ed1c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed1c-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="7ed1c-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
