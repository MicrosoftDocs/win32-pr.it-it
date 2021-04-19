---
description: Restituisce un oggetto DataUsage che indica l'utilizzo chiave valido del certificato.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'Metodo ICertificate2:: DataUsage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332929"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="673d1-103">Metodo ICertificate2:: DataUsage</span><span class="sxs-lookup"><span data-stu-id="673d1-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="673d1-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="673d1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="673d1-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="673d1-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="673d1-106">Il metodo di **utilizzo** della chiave restituisce un oggetto di [**utilizzo**](keyusage.md) chiavi che indica l'utilizzo chiave valido del certificato.</span><span class="sxs-lookup"><span data-stu-id="673d1-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="673d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="673d1-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="673d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="673d1-108">Parameters</span></span>

<span data-ttu-id="673d1-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="673d1-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="673d1-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="673d1-110">Requirements</span></span>



| <span data-ttu-id="673d1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="673d1-111">Requirement</span></span> | <span data-ttu-id="673d1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="673d1-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="673d1-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="673d1-113">End of client support</span></span><br/> | <span data-ttu-id="673d1-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="673d1-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="673d1-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="673d1-115">End of server support</span></span><br/> | <span data-ttu-id="673d1-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="673d1-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="673d1-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="673d1-117">Redistributable</span></span><br/>       | <span data-ttu-id="673d1-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="673d1-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="673d1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="673d1-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="673d1-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="673d1-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673d1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="673d1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673d1-122">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="673d1-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="673d1-123">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="673d1-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
