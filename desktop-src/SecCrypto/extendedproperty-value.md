---
description: Imposta o recupera i dati delle proprietà estese.
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: Proprietà ExtendedProperty. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ebbd977a107d92661110ceff02f3a5bb0bea191e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324844"
---
# <a name="extendedpropertyvalue-property"></a><span data-ttu-id="82cfd-103">Proprietà ExtendedProperty. Value</span><span class="sxs-lookup"><span data-stu-id="82cfd-103">ExtendedProperty.Value property</span></span>

<span data-ttu-id="82cfd-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="82cfd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="82cfd-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="82cfd-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="82cfd-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="82cfd-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="82cfd-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="82cfd-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="82cfd-108">La proprietà **value** imposta o recupera i dati delle proprietà estese.</span><span class="sxs-lookup"><span data-stu-id="82cfd-108">The **Value** property sets or retrieves the extended property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="82cfd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82cfd-109">Syntax</span></span>


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="82cfd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="82cfd-110">Property value</span></span>

<span data-ttu-id="82cfd-111">Dati della proprietà estesa, nel formato specificato da *EncodingType*.</span><span class="sxs-lookup"><span data-stu-id="82cfd-111">The extended property data, in the format specified by *EncodingType*.</span></span>

## <a name="requirements"></a><span data-ttu-id="82cfd-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82cfd-112">Requirements</span></span>



| <span data-ttu-id="82cfd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="82cfd-113">Requirement</span></span> | <span data-ttu-id="82cfd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="82cfd-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82cfd-115">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="82cfd-115">End of client support</span></span><br/> | <span data-ttu-id="82cfd-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82cfd-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="82cfd-117">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="82cfd-117">End of server support</span></span><br/> | <span data-ttu-id="82cfd-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82cfd-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="82cfd-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="82cfd-119">Redistributable</span></span><br/>       | <span data-ttu-id="82cfd-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="82cfd-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="82cfd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="82cfd-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="82cfd-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82cfd-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
