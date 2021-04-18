---
description: Aggiunge un oggetto certificato alla raccolta.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'Metodo ICertificates2:: Add'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330472"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="11971-103">Metodo ICertificates2:: Add</span><span class="sxs-lookup"><span data-stu-id="11971-103">ICertificates2::Add method</span></span>

<span data-ttu-id="11971-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="11971-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="11971-105">Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="11971-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="11971-106">Il metodo **Add** aggiunge un oggetto [**Certificate**](certificate.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="11971-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="11971-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="11971-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="11971-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11971-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="11971-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="11971-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11971-110">*Certificato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="11971-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11971-111">Oggetto [**certificato**](certificate.md) da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="11971-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11971-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11971-112">Return value</span></span>

<span data-ttu-id="11971-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="11971-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11971-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11971-114">Requirements</span></span>



| <span data-ttu-id="11971-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11971-115">Requirement</span></span> | <span data-ttu-id="11971-116">Valore</span><span class="sxs-lookup"><span data-stu-id="11971-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11971-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="11971-117">End of client support</span></span><br/> | <span data-ttu-id="11971-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11971-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="11971-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="11971-119">End of server support</span></span><br/> | <span data-ttu-id="11971-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11971-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="11971-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="11971-121">Redistributable</span></span><br/>       | <span data-ttu-id="11971-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="11971-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="11971-123">DLL</span><span class="sxs-lookup"><span data-stu-id="11971-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="11971-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11971-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
