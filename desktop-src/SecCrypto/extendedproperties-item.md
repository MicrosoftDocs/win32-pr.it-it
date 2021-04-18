---
description: La proprietà Item recupera un oggetto ExtendedProperty dalla raccolta. Si tratta della proprietà predefinita.
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: Proprietà ExtendedProperties. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328743"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="4d4e9-104">Proprietà ExtendedProperties. Item</span><span class="sxs-lookup"><span data-stu-id="4d4e9-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="4d4e9-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4d4e9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4d4e9-106">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d4e9-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="4d4e9-107">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d4e9-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="4d4e9-108">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="4d4e9-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="4d4e9-109">La proprietà **Item** recupera un oggetto [**ExtendedProperty**](extendedproperty.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d4e9-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="4d4e9-110">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="4d4e9-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4e9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d4e9-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="4d4e9-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4d4e9-112">Property value</span></span>

<span data-ttu-id="4d4e9-113">Oggetto [**ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa indicizzata della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d4e9-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4e9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d4e9-114">Requirements</span></span>



| <span data-ttu-id="4d4e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d4e9-115">Requirement</span></span> | <span data-ttu-id="4d4e9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4d4e9-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4e9-117">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d4e9-117">End of client support</span></span><br/> | <span data-ttu-id="4d4e9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d4e9-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d4e9-119">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4d4e9-119">End of server support</span></span><br/> | <span data-ttu-id="4d4e9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d4e9-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d4e9-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4d4e9-121">Redistributable</span></span><br/>       | <span data-ttu-id="4d4e9-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d4e9-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4d4e9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4d4e9-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4d4e9-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d4e9-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
