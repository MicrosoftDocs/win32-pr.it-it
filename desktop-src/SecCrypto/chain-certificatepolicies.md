---
description: Restituisce una raccolta OID che rappresenta i criteri di certificato OID validi per la catena.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'Metodo IChain2:: CertificatePolicies'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323969"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="861b8-103">Metodo IChain2:: CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="861b8-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="861b8-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="861b8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="861b8-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="861b8-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="861b8-106">Il metodo **CertificatePolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri di certificato OID validi per la catena.</span><span class="sxs-lookup"><span data-stu-id="861b8-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="861b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="861b8-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="861b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="861b8-108">Parameters</span></span>

<span data-ttu-id="861b8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="861b8-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="861b8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="861b8-110">Requirements</span></span>



| <span data-ttu-id="861b8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="861b8-111">Requirement</span></span> | <span data-ttu-id="861b8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="861b8-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="861b8-113">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="861b8-113">End of client support</span></span><br/> | <span data-ttu-id="861b8-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="861b8-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="861b8-115">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="861b8-115">End of server support</span></span><br/> | <span data-ttu-id="861b8-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="861b8-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="861b8-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="861b8-117">Redistributable</span></span><br/>       | <span data-ttu-id="861b8-118">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="861b8-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="861b8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="861b8-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="861b8-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="861b8-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
