---
description: Verifica la firma Authenticode sul codice firmato.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Metodo SignedCode. Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332836"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="e09e9-103">Metodo SignedCode. Verify</span><span class="sxs-lookup"><span data-stu-id="e09e9-103">SignedCode.Verify method</span></span>

<span data-ttu-id="e09e9-104">\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e09e9-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e09e9-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="e09e9-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="e09e9-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="e09e9-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="e09e9-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="e09e9-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="e09e9-108">Il metodo **Verify** verifica la firma Authenticode sul codice firmato.</span><span class="sxs-lookup"><span data-stu-id="e09e9-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09e9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e09e9-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e09e9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e09e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e09e9-111">*bUIAllowed* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e09e9-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e09e9-112">Valore booleano che specifica se una finestra di dialogo viene utilizzata per verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="e09e9-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="e09e9-113">Se è true, viene generata una finestra di dialogo per determinare se il codice è attendibile.</span><span class="sxs-lookup"><span data-stu-id="e09e9-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="e09e9-114">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="e09e9-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e09e9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e09e9-115">Return value</span></span>

<span data-ttu-id="e09e9-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e09e9-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09e9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e09e9-117">Requirements</span></span>



| <span data-ttu-id="e09e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e09e9-118">Requirement</span></span> | <span data-ttu-id="e09e9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e09e9-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e09e9-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e09e9-120">Redistributable</span></span><br/> | <span data-ttu-id="e09e9-121">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e09e9-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e09e9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e09e9-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="e09e9-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e09e9-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09e9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e09e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09e9-125">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="e09e9-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
