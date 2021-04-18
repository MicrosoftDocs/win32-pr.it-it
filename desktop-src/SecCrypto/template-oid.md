---
description: Recupera un oggetto OID che identifica l'oggetto modello.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Proprietà Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330599"
---
# <a name="templateoid-property"></a><span data-ttu-id="aaed6-103">Proprietà Template. OID</span><span class="sxs-lookup"><span data-stu-id="aaed6-103">Template.OID property</span></span>

<span data-ttu-id="aaed6-104">\[La proprietà **OID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="aaed6-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aaed6-105">Usare invece la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chiamando il costruttore che accetta un OID come parametro e quindi usare OID per il modello di certificato per recuperare il modello di estensione del certificato.\]</span><span class="sxs-lookup"><span data-stu-id="aaed6-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="aaed6-106">La proprietà **OID** recupera un oggetto [**OID**](oid.md) che identifica l'oggetto [**modello**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="aaed6-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="aaed6-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aaed6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaed6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaed6-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="aaed6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aaed6-109">Property value</span></span>

<span data-ttu-id="aaed6-110">Oggetto [**OID**](oid.md) che identifica l'oggetto [**modello**](template.md) .</span><span class="sxs-lookup"><span data-stu-id="aaed6-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaed6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaed6-111">Requirements</span></span>



| <span data-ttu-id="aaed6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaed6-112">Requirement</span></span> | <span data-ttu-id="aaed6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aaed6-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaed6-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="aaed6-114">Redistributable</span></span><br/> | <span data-ttu-id="aaed6-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="aaed6-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="aaed6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="aaed6-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="aaed6-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaed6-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaed6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaed6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaed6-119">**Modello**</span><span class="sxs-lookup"><span data-stu-id="aaed6-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
