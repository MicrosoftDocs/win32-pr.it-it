---
description: Restituisce una raccolta delle estensioni associate al certificato.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'Metodo ICertificate2:: Extensions'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329614"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="39614-103">Metodo ICertificate2:: Extensions</span><span class="sxs-lookup"><span data-stu-id="39614-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="39614-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39614-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="39614-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="39614-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="39614-106">Il metodo **Extensions** restituisce una raccolta delle estensioni associate al certificato.</span><span class="sxs-lookup"><span data-stu-id="39614-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="39614-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="39614-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="39614-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39614-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="39614-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="39614-109">Parameters</span></span>

<span data-ttu-id="39614-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="39614-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39614-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39614-111">Return value</span></span>

<span data-ttu-id="39614-112">Oggetto [**Extensions**](extensions.md) che rappresenta tutte le estensioni associate al certificato.</span><span class="sxs-lookup"><span data-stu-id="39614-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="39614-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39614-113">Requirements</span></span>



| <span data-ttu-id="39614-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39614-114">Requirement</span></span> | <span data-ttu-id="39614-115">Valore</span><span class="sxs-lookup"><span data-stu-id="39614-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39614-116">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="39614-116">End of client support</span></span><br/> | <span data-ttu-id="39614-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39614-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="39614-118">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="39614-118">End of server support</span></span><br/> | <span data-ttu-id="39614-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39614-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="39614-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="39614-120">Redistributable</span></span><br/>       | <span data-ttu-id="39614-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="39614-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39614-122">DLL</span><span class="sxs-lookup"><span data-stu-id="39614-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="39614-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39614-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
