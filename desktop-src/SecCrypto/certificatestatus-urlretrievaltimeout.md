---
description: Imposta o recupera l'intervallo di tempo prima che un URL venga determinato come irraggiungibile.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Proprietà CertificateStatus. UrlRetrievalTimeout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324137"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="ebe12-103">Proprietà CertificateStatus. UrlRetrievalTimeout</span><span class="sxs-lookup"><span data-stu-id="ebe12-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="ebe12-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ebe12-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ebe12-105">Usare invece la [**struttura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ebe12-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ebe12-106">La proprietà **UrlRetrievalTimeout** imposta o recupera l'intervallo di tempo prima che un URL venga determinato come irraggiungibile.</span><span class="sxs-lookup"><span data-stu-id="ebe12-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe12-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebe12-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="ebe12-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ebe12-108">Property value</span></span>

<span data-ttu-id="ebe12-109">Il numero di secondi prima che un URL venga determinato come irraggiungibile.</span><span class="sxs-lookup"><span data-stu-id="ebe12-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe12-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebe12-110">Remarks</span></span>

<span data-ttu-id="ebe12-111">Se questa proprietà non è impostata, il timeout predefinito è 15 secondi.</span><span class="sxs-lookup"><span data-stu-id="ebe12-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe12-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebe12-112">Requirements</span></span>



| <span data-ttu-id="ebe12-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe12-113">Requirement</span></span> | <span data-ttu-id="ebe12-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ebe12-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe12-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ebe12-115">End of client support</span></span><br/> | <span data-ttu-id="ebe12-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebe12-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ebe12-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ebe12-117">End of server support</span></span><br/> | <span data-ttu-id="ebe12-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebe12-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebe12-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ebe12-119">Redistributable</span></span><br/>       | <span data-ttu-id="ebe12-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebe12-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ebe12-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ebe12-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ebe12-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebe12-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
