---
description: La proprietà FileName imposta o Recupera il percorso del file eseguibile. Si tratta della proprietà predefinita.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Proprietà SignedCode. FileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333560"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="36bfd-104">Proprietà SignedCode. FileName</span><span class="sxs-lookup"><span data-stu-id="36bfd-104">SignedCode.FileName property</span></span>

<span data-ttu-id="36bfd-105">\[La proprietà **filename** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="36bfd-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="36bfd-106">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="36bfd-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="36bfd-107">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="36bfd-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="36bfd-108">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="36bfd-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="36bfd-109">La proprietà **filename** imposta o Recupera il percorso del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="36bfd-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="36bfd-110">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="36bfd-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="36bfd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36bfd-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="36bfd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="36bfd-112">Property value</span></span>

<span data-ttu-id="36bfd-113">Percorso del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="36bfd-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="36bfd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="36bfd-114">Remarks</span></span>

<span data-ttu-id="36bfd-115">Se il valore della proprietà **filename** viene modificato, lo stato dell'intero oggetto [**SignedCode**](signedcode.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="36bfd-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="36bfd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36bfd-116">Requirements</span></span>



| <span data-ttu-id="36bfd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="36bfd-117">Requirement</span></span> | <span data-ttu-id="36bfd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="36bfd-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36bfd-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="36bfd-119">Redistributable</span></span><br/> | <span data-ttu-id="36bfd-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="36bfd-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="36bfd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="36bfd-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="36bfd-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36bfd-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36bfd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36bfd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bfd-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="36bfd-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
