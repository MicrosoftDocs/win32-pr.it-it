---
description: Recupera il firmatario del file eseguibile firmato.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Proprietà SignedCode. Signer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330271"
---
# <a name="signedcodesigner-property"></a><span data-ttu-id="08ea6-103">Proprietà SignedCode. Signer</span><span class="sxs-lookup"><span data-stu-id="08ea6-103">SignedCode.Signer property</span></span>

<span data-ttu-id="08ea6-104">\[La proprietà **firmatario** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="08ea6-104">\[The **Signer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08ea6-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="08ea6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="08ea6-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="08ea6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="08ea6-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="08ea6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="08ea6-108">La proprietà **Signer** Recupera il firmatario del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="08ea6-108">The **Signer** property retrieves the signer of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ea6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08ea6-109">Syntax</span></span>


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a><span data-ttu-id="08ea6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="08ea6-110">Property value</span></span>

<span data-ttu-id="08ea6-111">Oggetto [**firmatario**](signer.md) che fornisce l'accesso al firmatario del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="08ea6-111">A [**Signer**](signer.md) object that provides access to the signer of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ea6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08ea6-112">Requirements</span></span>



| <span data-ttu-id="08ea6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ea6-113">Requirement</span></span> | <span data-ttu-id="08ea6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="08ea6-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08ea6-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="08ea6-115">Redistributable</span></span><br/> | <span data-ttu-id="08ea6-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="08ea6-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08ea6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="08ea6-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="08ea6-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08ea6-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ea6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08ea6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ea6-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="08ea6-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
