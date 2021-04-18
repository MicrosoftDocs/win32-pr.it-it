---
description: Crea una firma di timestamp Authenticode sul file eseguibile firmato specificato nella proprietà SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. timestamp, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327895"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="53f86-103">SignedCode. timestamp, metodo</span><span class="sxs-lookup"><span data-stu-id="53f86-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="53f86-104">\[Il metodo **timestamp** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="53f86-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="53f86-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="53f86-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="53f86-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="53f86-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="53f86-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="53f86-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="53f86-108">Il metodo **timestamp** crea una firma timestamp Authenticode sul file eseguibile firmato specificato nella proprietà **SignedCode. FileName** .</span><span class="sxs-lookup"><span data-stu-id="53f86-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="53f86-109">Questo timestamp è una firma del contatore nel file eseguibile firmato eseguito da un'autorità di timestamp.</span><span class="sxs-lookup"><span data-stu-id="53f86-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f86-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f86-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="53f86-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f86-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f86-112">*URL* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="53f86-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f86-113">Stringa che contiene l'URL del server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="53f86-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f86-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f86-114">Return value</span></span>

<span data-ttu-id="53f86-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="53f86-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f86-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f86-116">Remarks</span></span>

<span data-ttu-id="53f86-117">Un timestamp estende la validità di un certificato verificando che il file eseguibile sia stato firmato al momento del timestamp.</span><span class="sxs-lookup"><span data-stu-id="53f86-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="53f86-118">Prima di poter chiamare questo metodo, è necessario specificare il file eseguibile firmato per il timestamp, nella proprietà **SignedCode. FileName** , ed è necessario chiamare il metodo [**SignedCode. Sign**](signedcode-sign.md) per firmare il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="53f86-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="53f86-119">Se il file eseguibile firmato è già contrassegnato come timestamp, questo metodo sovrascrive il timestamp esistente.</span><span class="sxs-lookup"><span data-stu-id="53f86-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f86-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f86-120">Requirements</span></span>



| <span data-ttu-id="53f86-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f86-121">Requirement</span></span> | <span data-ttu-id="53f86-122">Valore</span><span class="sxs-lookup"><span data-stu-id="53f86-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f86-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="53f86-123">Redistributable</span></span><br/> | <span data-ttu-id="53f86-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="53f86-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="53f86-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53f86-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="53f86-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f86-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f86-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f86-128">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="53f86-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
