---
description: L'interfaccia IWordInfo è un componente di risorse del linguaggio specifico per il giapponese. L'oggetto analizza il testo e identifica le singole parole, restituendo le parole nella stringa o restituisce le forme del dizionario (radice) delle parole nel testo della stringa.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interfaccia IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522977"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="c4723-104">Interfaccia IWordInfo</span><span class="sxs-lookup"><span data-stu-id="c4723-104">IWordInfo interface</span></span>

<span data-ttu-id="c4723-105">\[Questa interfaccia è obsoleta e non è supportata in Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="c4723-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="c4723-106">L'interfaccia **IWordInfo** è un componente di risorse del linguaggio specifico per il giapponese.</span><span class="sxs-lookup"><span data-stu-id="c4723-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="c4723-107">L'oggetto analizza il testo e identifica le singole parole, restituendo le parole nella stringa o restituisce le forme del dizionario (radice) delle parole nel testo della stringa.</span><span class="sxs-lookup"><span data-stu-id="c4723-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="c4723-108">Membri</span><span class="sxs-lookup"><span data-stu-id="c4723-108">Members</span></span>

<span data-ttu-id="c4723-109">L'interfaccia **IWordInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4723-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4723-110">**IWordInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c4723-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="c4723-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4723-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4723-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4723-112">Methods</span></span>

<span data-ttu-id="c4723-113">L'interfaccia **IWordInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c4723-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="c4723-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="c4723-114">Method</span></span>        | <span data-ttu-id="c4723-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4723-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4723-116">**BreakText**</span><span class="sxs-lookup"><span data-stu-id="c4723-116">**BreakText**</span></span> | <span data-ttu-id="c4723-117">Analizza il testo per identificare le parole e fornisce i risultati all'oggetto [WordSink](/previous-versions//ms691570(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c4723-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4723-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4723-118">Remarks</span></span>

<span data-ttu-id="c4723-119">Questa interfaccia viene utilizzata per recuperare le interruzioni di parola giapponesi o i form del dizionario per il testo da analizzare.</span><span class="sxs-lookup"><span data-stu-id="c4723-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="c4723-120">Il formato del dizionario di una parola è il formato uninflected della parola.</span><span class="sxs-lookup"><span data-stu-id="c4723-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4723-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4723-121">Requirements</span></span>



| <span data-ttu-id="c4723-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4723-122">Requirement</span></span> | <span data-ttu-id="c4723-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c4723-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4723-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4723-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4723-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c4723-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c4723-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4723-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4723-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4723-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4723-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c4723-128">End of client support</span></span><br/>    | <span data-ttu-id="c4723-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4723-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c4723-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c4723-130">End of server support</span></span><br/>    | <span data-ttu-id="c4723-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4723-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c4723-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c4723-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4723-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4723-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4723-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4723-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4723-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="c4723-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="c4723-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4723-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
