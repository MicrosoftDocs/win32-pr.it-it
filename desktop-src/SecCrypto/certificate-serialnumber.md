---
description: Recupera una stringa che contiene il numero di serie del certificato.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Proprietà Certificate. SerialNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327095"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="a1252-103">Proprietà Certificate. SerialNumber</span><span class="sxs-lookup"><span data-stu-id="a1252-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="a1252-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1252-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a1252-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a1252-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a1252-106">La proprietà **serialNumber** recupera una stringa che contiene il numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="a1252-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="a1252-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a1252-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1252-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1252-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="a1252-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a1252-109">Property value</span></span>

<span data-ttu-id="a1252-110">Stringa che contiene il numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="a1252-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1252-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1252-111">Requirements</span></span>



| <span data-ttu-id="a1252-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1252-112">Requirement</span></span> | <span data-ttu-id="a1252-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a1252-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1252-114">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a1252-114">End of client support</span></span><br/> | <span data-ttu-id="a1252-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1252-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1252-116">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a1252-116">End of server support</span></span><br/> | <span data-ttu-id="a1252-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1252-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1252-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a1252-118">Redistributable</span></span><br/>       | <span data-ttu-id="a1252-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1252-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a1252-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a1252-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a1252-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1252-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
