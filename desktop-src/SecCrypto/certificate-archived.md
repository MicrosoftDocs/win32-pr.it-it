---
description: Imposta o recupera un valore booleano che indica se il certificato è archiviato.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Proprietà Certificate. Archived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333781"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="b978e-103">Proprietà Certificate. Archived</span><span class="sxs-lookup"><span data-stu-id="b978e-103">Certificate.Archived property</span></span>

<span data-ttu-id="b978e-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b978e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b978e-105">Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b978e-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b978e-106">La proprietà **archiviata** imposta o recupera un valore booleano che indica se il certificato è archiviato.</span><span class="sxs-lookup"><span data-stu-id="b978e-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="b978e-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b978e-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b978e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b978e-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b978e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b978e-109">Property value</span></span>

<span data-ttu-id="b978e-110">Valore booleano che indica se il certificato è archiviato.</span><span class="sxs-lookup"><span data-stu-id="b978e-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="b978e-111">Se **true**, il certificato viene archiviato.</span><span class="sxs-lookup"><span data-stu-id="b978e-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="b978e-112">Si noti che la modifica del valore da **false** a **true** archivia il certificato.</span><span class="sxs-lookup"><span data-stu-id="b978e-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="b978e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b978e-113">Remarks</span></span>

<span data-ttu-id="b978e-114">Questa proprietà genera CAPICOM \_ E \_ non \_ è consentita quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="b978e-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="b978e-115">Un certificato archiviato non è visibile nell'interfaccia utente di gestione certificati.</span><span class="sxs-lookup"><span data-stu-id="b978e-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="b978e-116">I certificati archiviati, inoltre, non verranno inclusi nel metodo [**Store. Open**](store-open.md) , a meno che non \_ \_ \_ \_ sia specificato Archived Store.</span><span class="sxs-lookup"><span data-stu-id="b978e-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b978e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b978e-117">Requirements</span></span>



| <span data-ttu-id="b978e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b978e-118">Requirement</span></span> | <span data-ttu-id="b978e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b978e-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b978e-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b978e-120">End of client support</span></span><br/> | <span data-ttu-id="b978e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b978e-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b978e-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b978e-122">End of server support</span></span><br/> | <span data-ttu-id="b978e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b978e-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b978e-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b978e-124">Redistributable</span></span><br/>       | <span data-ttu-id="b978e-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b978e-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b978e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b978e-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b978e-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b978e-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
