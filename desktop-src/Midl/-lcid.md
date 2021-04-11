---
title: opzione/LCID
description: L'opzione del compilatore MIDL/LCID consente di usare i caratteri internazionali nei file di input, nei nomi file e nei percorsi di directory.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /LCID switch MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334559"
---
# <a name="lcid-switch"></a><span data-ttu-id="448ca-104">opzione/LCID</span><span class="sxs-lookup"><span data-stu-id="448ca-104">/lcid switch</span></span>

<span data-ttu-id="448ca-105">L'opzione del compilatore MIDL **/LCID** consente di usare i caratteri internazionali nei file di input, nei nomi file e nei percorsi di directory.</span><span class="sxs-lookup"><span data-stu-id="448ca-105">The **/lcid** MIDL compiler option lets you use international characters in your input files, file names, and directory paths.</span></span>

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a><span data-ttu-id="448ca-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="448ca-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="448ca-107">*localeID*</span><span class="sxs-lookup"><span data-stu-id="448ca-107">*localeID*</span></span> 
</dt> <dd>

<span data-ttu-id="448ca-108">Specifica l'identificatore delle impostazioni locali a 32 bit utilizzato nel supporto della lingua nazionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="448ca-108">Specifies the 32-bit locale identifier used in Windows National Language Support.</span></span> <span data-ttu-id="448ca-109">L'identificatore delle impostazioni locali deve essere specificato in decimale.</span><span class="sxs-lookup"><span data-stu-id="448ca-109">The locale identifier should be specified in decimal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="448ca-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="448ca-110">Remarks</span></span>

<span data-ttu-id="448ca-111">Nei file di input è possibile utilizzare commenti, stringhe, HelpStrings e identificatori localizzati.</span><span class="sxs-lookup"><span data-stu-id="448ca-111">Within the input files, you can use localized comments, strings, helpstrings and identifiers.</span></span> <span data-ttu-id="448ca-112">In particolare, l'opzione **/LCID** fornisce un supporto DBCS completo, per rappresentare lingue asiatiche quali giapponese, cinese e coreano.</span><span class="sxs-lookup"><span data-stu-id="448ca-112">In particular, the **/lcid** switch provides full DBCS support, to represent Asian languages such as Japanese, Chinese, and Korean.</span></span>

> [!Note]  
> <span data-ttu-id="448ca-113">L'opzione **/LCID** è disponibile con MIDL versione 3.01.75 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="448ca-113">The **/lcid** switch is available with MIDL version 3.01.75 and later.</span></span>

 

## <a name="examples"></a><span data-ttu-id="448ca-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="448ca-114">Examples</span></span>

<span data-ttu-id="448ca-115">**MIDL/LCID 1041 iface. idl**</span><span class="sxs-lookup"><span data-stu-id="448ca-115">**midl /lcid 1041 iface.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="448ca-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="448ca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448ca-117">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="448ca-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="448ca-118">**LCID**</span><span class="sxs-lookup"><span data-stu-id="448ca-118">**lcid**</span></span>](lcid.md)
</dt> </dl>

 

 




