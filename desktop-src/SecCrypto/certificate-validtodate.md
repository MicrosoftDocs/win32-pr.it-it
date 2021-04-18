---
description: Recupera la data di fine per la validità del certificato.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Proprietà Certificate. ValidToDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328000"
---
# <a name="certificatevalidtodate-property"></a><span data-ttu-id="eec36-103">Proprietà Certificate. ValidToDate</span><span class="sxs-lookup"><span data-stu-id="eec36-103">Certificate.ValidToDate property</span></span>

<span data-ttu-id="eec36-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eec36-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="eec36-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="eec36-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="eec36-106">La proprietà **ValidToDate** recupera la data di fine per la validità del certificato.</span><span class="sxs-lookup"><span data-stu-id="eec36-106">The **ValidToDate** property retrieves the ending date for the validity of the certificate.</span></span>

<span data-ttu-id="eec36-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="eec36-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec36-108">Syntax</span></span>


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a><span data-ttu-id="eec36-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="eec36-109">Property value</span></span>

<span data-ttu-id="eec36-110">Data che indica la data di fine per la validità del certificato.</span><span class="sxs-lookup"><span data-stu-id="eec36-110">A date that indicates the ending date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec36-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec36-111">Requirements</span></span>



| <span data-ttu-id="eec36-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec36-112">Requirement</span></span> | <span data-ttu-id="eec36-113">Valore</span><span class="sxs-lookup"><span data-stu-id="eec36-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec36-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="eec36-114">End of client support</span></span><br/> | <span data-ttu-id="eec36-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eec36-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="eec36-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="eec36-116">End of server support</span></span><br/> | <span data-ttu-id="eec36-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eec36-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="eec36-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="eec36-118">Redistributable</span></span><br/>       | <span data-ttu-id="eec36-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="eec36-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eec36-120">DLL</span><span class="sxs-lookup"><span data-stu-id="eec36-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="eec36-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eec36-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec36-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec36-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec36-123">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="eec36-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
