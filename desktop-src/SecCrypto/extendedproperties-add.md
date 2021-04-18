---
description: Aggiunge una proprietà estesa alla raccolta.
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: Metodo ExtendedProperties. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330130"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="1057a-103">Metodo ExtendedProperties. Add</span><span class="sxs-lookup"><span data-stu-id="1057a-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="1057a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1057a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1057a-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare la funzione API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e ottenere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="1057a-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="1057a-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="1057a-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1057a-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="1057a-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1057a-108">Il metodo **Add** aggiunge una proprietà estesa alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="1057a-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1057a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1057a-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="1057a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1057a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1057a-111">*valProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1057a-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1057a-112">Oggetto [**ExtendedProperty**](extendedproperty.md) che rappresenta la proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="1057a-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1057a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1057a-113">Return value</span></span>

<span data-ttu-id="1057a-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1057a-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1057a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1057a-115">Requirements</span></span>



| <span data-ttu-id="1057a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1057a-116">Requirement</span></span> | <span data-ttu-id="1057a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1057a-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1057a-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1057a-118">End of client support</span></span><br/> | <span data-ttu-id="1057a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1057a-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1057a-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1057a-120">End of server support</span></span><br/> | <span data-ttu-id="1057a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1057a-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1057a-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1057a-122">Redistributable</span></span><br/>       | <span data-ttu-id="1057a-123">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="1057a-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1057a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1057a-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1057a-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1057a-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
