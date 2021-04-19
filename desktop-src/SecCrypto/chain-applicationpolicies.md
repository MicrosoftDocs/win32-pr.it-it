---
description: Restituisce una raccolta OID che rappresenta i criteri dell'applicazione OID validi per la catena.
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: 'Metodo IChain2:: ApplicationPolicies'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a90eb7a493bfe81f5c4a38f773b0307380002b6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333156"
---
# <a name="ichain2applicationpolicies-method"></a><span data-ttu-id="ff6d4-103">Metodo IChain2:: ApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="ff6d4-103">IChain2::ApplicationPolicies method</span></span>

<span data-ttu-id="ff6d4-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ff6d4-105">Usare invece la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ff6d4-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ff6d4-106">Il metodo **ApplicationPolicies** restituisce una raccolta [**OID**](oids.md) che rappresenta i criteri dell'applicazione OID validi per la catena.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span>

<span data-ttu-id="ff6d4-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff6d4-108">Syntax</span></span>


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="ff6d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff6d4-109">Parameters</span></span>

<span data-ttu-id="ff6d4-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ff6d4-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6d4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff6d4-111">Requirements</span></span>



| <span data-ttu-id="ff6d4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff6d4-112">Requirement</span></span> | <span data-ttu-id="ff6d4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ff6d4-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6d4-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ff6d4-114">End of client support</span></span><br/> | <span data-ttu-id="ff6d4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff6d4-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff6d4-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ff6d4-116">End of server support</span></span><br/> | <span data-ttu-id="ff6d4-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff6d4-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff6d4-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ff6d4-118">Redistributable</span></span><br/>       | <span data-ttu-id="ff6d4-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff6d4-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ff6d4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ff6d4-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ff6d4-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff6d4-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
