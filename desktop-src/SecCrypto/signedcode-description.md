---
description: Imposta o recupera la descrizione del file eseguibile firmato.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Proprietà SignedCode. Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329462"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="df85b-103">Proprietà SignedCode. Description</span><span class="sxs-lookup"><span data-stu-id="df85b-103">SignedCode.Description property</span></span>

<span data-ttu-id="df85b-104">\[La proprietà **Description** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="df85b-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="df85b-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="df85b-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="df85b-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="df85b-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="df85b-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="df85b-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="df85b-108">La proprietà **Description** imposta o recupera la descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="df85b-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="df85b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df85b-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="df85b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="df85b-110">Property value</span></span>

<span data-ttu-id="df85b-111">Descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="df85b-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="df85b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="df85b-112">Remarks</span></span>

<span data-ttu-id="df85b-113">La descrizione è il testo visualizzato nella finestra di dialogo di verifica Authenticode.</span><span class="sxs-lookup"><span data-stu-id="df85b-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="df85b-114">Il testo deve descrivere il file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="df85b-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="df85b-115">Se questa proprietà è **null**, nella finestra di dialogo verrà visualizzato il nome del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="df85b-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="df85b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df85b-116">Requirements</span></span>



| <span data-ttu-id="df85b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df85b-117">Requirement</span></span> | <span data-ttu-id="df85b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="df85b-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df85b-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="df85b-119">Redistributable</span></span><br/> | <span data-ttu-id="df85b-120">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="df85b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="df85b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="df85b-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="df85b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df85b-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df85b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df85b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df85b-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="df85b-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
