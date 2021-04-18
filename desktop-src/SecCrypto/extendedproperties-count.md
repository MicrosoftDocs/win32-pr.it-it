---
description: Recupera il numero di oggetti ExtendedProperty nell'insieme.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: Proprietà ExtendedProperties. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328746"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="c4033-103">Proprietà ExtendedProperties. Count</span><span class="sxs-lookup"><span data-stu-id="c4033-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="c4033-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c4033-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c4033-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4033-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="c4033-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4033-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="c4033-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="c4033-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="c4033-108">La proprietà **count** Recupera il numero di oggetti [**ExtendedProperty**](extendedproperty.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="c4033-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4033-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4033-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="c4033-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c4033-110">Property value</span></span>

<span data-ttu-id="c4033-111">Numero di oggetti [**ExtendedProperty**](extendedproperty.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="c4033-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4033-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4033-112">Requirements</span></span>



| <span data-ttu-id="c4033-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4033-113">Requirement</span></span> | <span data-ttu-id="c4033-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c4033-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4033-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c4033-115">End of client support</span></span><br/> | <span data-ttu-id="c4033-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4033-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4033-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c4033-117">End of server support</span></span><br/> | <span data-ttu-id="c4033-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4033-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4033-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c4033-119">Redistributable</span></span><br/>       | <span data-ttu-id="c4033-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4033-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c4033-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c4033-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c4033-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4033-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
