---
description: La proprietà TimeStamp Recupera il timestamp del file eseguibile firmato.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Proprietà SignedCode. TimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332838"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="972e1-103">Proprietà SignedCode. TimeStamp</span><span class="sxs-lookup"><span data-stu-id="972e1-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="972e1-104">\[La proprietà **timestamp** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="972e1-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="972e1-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="972e1-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="972e1-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="972e1-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="972e1-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="972e1-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="972e1-108">La proprietà **timestamp** Recupera il timestamp del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="972e1-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="972e1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="972e1-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="972e1-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="972e1-110">Property value</span></span>

<span data-ttu-id="972e1-111">Oggetto [**firmatario**](signer.md) che fornisce l'accesso al timestamp del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="972e1-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="972e1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="972e1-112">Requirements</span></span>



| <span data-ttu-id="972e1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="972e1-113">Requirement</span></span> | <span data-ttu-id="972e1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="972e1-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="972e1-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="972e1-115">Redistributable</span></span><br/> | <span data-ttu-id="972e1-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="972e1-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="972e1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="972e1-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="972e1-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972e1-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="972e1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="972e1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972e1-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="972e1-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
