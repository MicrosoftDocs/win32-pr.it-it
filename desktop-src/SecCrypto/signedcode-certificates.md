---
description: Recupera la raccolta di certificati nel file eseguibile firmato.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Proprietà SignedCode. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329463"
---
# <a name="signedcodecertificates-property"></a><span data-ttu-id="d726f-103">Proprietà SignedCode. Certificates</span><span class="sxs-lookup"><span data-stu-id="d726f-103">SignedCode.Certificates property</span></span>

<span data-ttu-id="d726f-104">\[La proprietà **Certificates** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d726f-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d726f-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="d726f-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="d726f-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="d726f-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="d726f-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="d726f-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="d726f-108">La proprietà **Certificates** recupera la raccolta di certificati nel file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="d726f-108">The **Certificates** property retrieves the collection of certificates in the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d726f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d726f-109">Syntax</span></span>


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="d726f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d726f-110">Property value</span></span>

<span data-ttu-id="d726f-111">Raccolta di [**certificati**](certificates.md) che contiene tutti i certificati nel file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="d726f-111">The [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d726f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d726f-112">Requirements</span></span>



| <span data-ttu-id="d726f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d726f-113">Requirement</span></span> | <span data-ttu-id="d726f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d726f-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d726f-115">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d726f-115">Redistributable</span></span><br/> | <span data-ttu-id="d726f-116">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="d726f-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d726f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d726f-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="d726f-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d726f-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d726f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d726f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d726f-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="d726f-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
