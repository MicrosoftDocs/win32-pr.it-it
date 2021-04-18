---
description: Restituisce un oggetto BasicConstraints che rappresenta l'estensione dei vincoli di base del certificato.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'Metodo ICertificate2:: BasicConstraints'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333780"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="7bb3b-103">Metodo ICertificate2:: BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="7bb3b-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="7bb3b-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7bb3b-105">Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7bb3b-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7bb3b-106">Il metodo **BasicConstraints** restituisce un oggetto [**BasicConstraints**](basicconstraints.md) che rappresenta l'estensione dei vincoli di base del certificato.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bb3b-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="7bb3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bb3b-108">Parameters</span></span>

<span data-ttu-id="7bb3b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bb3b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bb3b-110">Return value</span></span>

<span data-ttu-id="7bb3b-111">Oggetto [**BasicConstraints**](basicconstraints.md) che rappresenta l'estensione dei vincoli di base del certificato.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb3b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bb3b-112">Requirements</span></span>



| <span data-ttu-id="7bb3b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb3b-113">Requirement</span></span> | <span data-ttu-id="7bb3b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7bb3b-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb3b-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7bb3b-115">End of client support</span></span><br/> | <span data-ttu-id="7bb3b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bb3b-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7bb3b-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7bb3b-117">End of server support</span></span><br/> | <span data-ttu-id="7bb3b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bb3b-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7bb3b-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7bb3b-119">Redistributable</span></span><br/>       | <span data-ttu-id="7bb3b-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bb3b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7bb3b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb3b-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7bb3b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bb3b-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
