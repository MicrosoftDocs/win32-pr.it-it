---
description: Imposta o recupera l'URL di una descrizione del file eseguibile firmato.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Proprietà SignedCode. DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325460"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="57116-103">Proprietà SignedCode. DescriptionURL</span><span class="sxs-lookup"><span data-stu-id="57116-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="57116-104">\[La proprietà **DescriptionURL** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="57116-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="57116-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="57116-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="57116-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="57116-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="57116-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="57116-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="57116-108">La proprietà **DescriptionURL** imposta o recupera l'URL di una descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="57116-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="57116-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57116-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="57116-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="57116-110">Property value</span></span>

<span data-ttu-id="57116-111">URL di una descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="57116-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="57116-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="57116-112">Remarks</span></span>

<span data-ttu-id="57116-113">**DescriptionURL** è l'URL a cui è collegata la [**Descrizione**](signedcode-description.md) visualizzata nella finestra di dialogo di verifica Authenticode.</span><span class="sxs-lookup"><span data-stu-id="57116-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="57116-114">Se questa proprietà è **null**, la **Descrizione** non funzionerà come collegamento.</span><span class="sxs-lookup"><span data-stu-id="57116-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="57116-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57116-115">Requirements</span></span>



| <span data-ttu-id="57116-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="57116-116">Requirement</span></span> | <span data-ttu-id="57116-117">Valore</span><span class="sxs-lookup"><span data-stu-id="57116-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57116-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="57116-118">Redistributable</span></span><br/> | <span data-ttu-id="57116-119">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="57116-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="57116-120">DLL</span><span class="sxs-lookup"><span data-stu-id="57116-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="57116-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57116-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57116-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57116-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57116-123">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="57116-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
