---
description: Recupera una stringa che contiene il nome dell'autorità emittente del certificato.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Proprietà Certificate. IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328005"
---
# <a name="certificateissuername-property"></a><span data-ttu-id="0054d-103">Proprietà Certificate. IssuerName</span><span class="sxs-lookup"><span data-stu-id="0054d-103">Certificate.IssuerName property</span></span>

<span data-ttu-id="0054d-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0054d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0054d-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0054d-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0054d-106">La proprietà **IssuerName** recupera una stringa che contiene il nome dell'autorità emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="0054d-106">The **IssuerName** property retrieves a string that contains the name of the certificate issuer.</span></span>

<span data-ttu-id="0054d-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0054d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0054d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0054d-108">Syntax</span></span>


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a><span data-ttu-id="0054d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0054d-109">Property value</span></span>

<span data-ttu-id="0054d-110">Stringa che contiene il nome dell'autorità emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="0054d-110">String that contains the name of the certificate issuer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0054d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0054d-111">Requirements</span></span>



| <span data-ttu-id="0054d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0054d-112">Requirement</span></span> | <span data-ttu-id="0054d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0054d-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0054d-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0054d-114">End of client support</span></span><br/> | <span data-ttu-id="0054d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0054d-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0054d-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0054d-116">End of server support</span></span><br/> | <span data-ttu-id="0054d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0054d-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0054d-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0054d-118">Redistributable</span></span><br/>       | <span data-ttu-id="0054d-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="0054d-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0054d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0054d-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0054d-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0054d-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
