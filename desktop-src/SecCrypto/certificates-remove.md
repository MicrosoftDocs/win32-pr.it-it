---
description: Rimuove un singolo oggetto certificato dalla raccolta.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Metodo ICertificates2:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331906"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="ebf24-103">Metodo ICertificates2:: Remove</span><span class="sxs-lookup"><span data-stu-id="ebf24-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="ebf24-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebf24-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ebf24-105">Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ebf24-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ebf24-106">Il metodo **Remove** rimuove un singolo oggetto [**Certificate**](certificate.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="ebf24-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="ebf24-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="ebf24-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf24-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebf24-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="ebf24-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebf24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf24-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ebf24-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf24-111">Valore di indice per l'oggetto [**certificato**](certificate.md) da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ebf24-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="ebf24-112">Questo parametro può essere uno dei seguenti tipi possibili.</span><span class="sxs-lookup"><span data-stu-id="ebf24-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="ebf24-113">Type</span><span class="sxs-lookup"><span data-stu-id="ebf24-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="ebf24-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ebf24-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="ebf24-115">\* \* \* \* <dt>Long \* \*</dt> \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="ebf24-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="ebf24-116">L'oggetto [**certificato**](certificate.md) in corrispondenza dell'indice specificato nella raccolta viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="ebf24-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="ebf24-117">\* \* \* \* <dt>Stringa \* \*</dt> \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="ebf24-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="ebf24-118">Il primo oggetto [**certificato**](certificate.md) della raccolta che corrisponde all'identificazione personale [*SHA-1*](../secgloss/s-gly.md) contenuto nella stringa specificata viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="ebf24-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="ebf24-119"><dt>**[**Certificato**](certificate.md)**</dt> di <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ebf24-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="ebf24-120">Il primo oggetto [**certificato**](certificate.md) della raccolta che corrisponde all'oggetto **certificato** specificato viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="ebf24-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf24-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebf24-121">Return value</span></span>

<span data-ttu-id="ebf24-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ebf24-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf24-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebf24-123">Requirements</span></span>



| <span data-ttu-id="ebf24-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf24-124">Requirement</span></span> | <span data-ttu-id="ebf24-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ebf24-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf24-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ebf24-126">End of client support</span></span><br/> | <span data-ttu-id="ebf24-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebf24-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ebf24-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ebf24-128">End of server support</span></span><br/> | <span data-ttu-id="ebf24-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebf24-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebf24-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ebf24-130">Redistributable</span></span><br/>       | <span data-ttu-id="ebf24-131">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebf24-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ebf24-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf24-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ebf24-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf24-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
