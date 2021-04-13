---
description: La funzione di esportazione ParserAutoInstallInfo identifica il parser o i parser che si trovano in una DLL. ParserAutoInstallInfo deve essere implementato in tutte le dll del parser.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Funzione di callback ParserAutoInstallInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342741"
---
# <a name="parserautoinstallinfo-callback-function"></a><span data-ttu-id="41358-104">Funzione di callback ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="41358-104">ParserAutoInstallInfo callback function</span></span>

<span data-ttu-id="41358-105">La funzione di esportazione **ParserAutoInstallInfo** identifica il parser o i parser che si trovano in una dll.</span><span class="sxs-lookup"><span data-stu-id="41358-105">The **ParserAutoInstallInfo** export function identifies the parser, or parsers that are located in a DLL.</span></span> <span data-ttu-id="41358-106">**ParserAutoInstallInfo** deve essere implementato in tutte le dll del parser.</span><span class="sxs-lookup"><span data-stu-id="41358-106">**ParserAutoInstallInfo** should be implemented in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="41358-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41358-107">Syntax</span></span>


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a><span data-ttu-id="41358-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41358-108">Parameters</span></span>

<span data-ttu-id="41358-109">Questa funzione di callback non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="41358-109">This callback function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41358-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41358-110">Return value</span></span>

<span data-ttu-id="41358-111">Se la funzione ha esito positivo, il valore restituito è una struttura [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) che descrive i parser nella dll.</span><span class="sxs-lookup"><span data-stu-id="41358-111">If the function is successful, the return value is a [PF\_PARSERDLLINFO](pf-parserdllinfo.md) structure that describes the parsers in the DLL.</span></span>

<span data-ttu-id="41358-112">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="41358-112">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41358-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="41358-113">Remarks</span></span>

<span data-ttu-id="41358-114">Quando Network Monitor viene caricato per la prima volta, viene chiamato **ParserAutoInstallInfo** (se esiste) per installare automaticamente ogni parser e quindi vengono enumerate tutte le dll del parser nella sottodirectory del parser.</span><span class="sxs-lookup"><span data-stu-id="41358-114">When Network Monitor loads for the first time, it calls **ParserAutoInstallInfo** (if it exists) to automatically install each parser, and then enumerate all the parser DLLs in the parser subdirectory.</span></span>

<span data-ttu-id="41358-115">Le informazioni restituite nella struttura **PF \_ PARSERDLLINFO** includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="41358-115">The information returned in the **PF\_PARSERDLLINFO** structure includes the following:</span></span>

-   <span data-ttu-id="41358-116">Numero di parser nella DLL (in genere uno).</span><span class="sxs-lookup"><span data-stu-id="41358-116">The number of parsers in the DLL (typically one).</span></span>
-   <span data-ttu-id="41358-117">Nome e breve descrizione del protocollo rilevato da ogni parser.</span><span class="sxs-lookup"><span data-stu-id="41358-117">The name and a brief description of the protocol that each parser detects.</span></span>
-   <span data-ttu-id="41358-118">File della guida facoltativo per ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="41358-118">An optional Help file for each protocol.</span></span>
-   <span data-ttu-id="41358-119">Protocolli che precedono ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="41358-119">The protocols that precede each protocol.</span></span>
-   <span data-ttu-id="41358-120">Protocolli che seguono ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="41358-120">The protocols that follow each protocol.</span></span>

<span data-ttu-id="41358-121">Ogni DLL del parser deve contenere un parser.</span><span class="sxs-lookup"><span data-stu-id="41358-121">Each parser DLL should contain one parser.</span></span> <span data-ttu-id="41358-122">Tuttavia, Network Monitor consente di creare una DLL che contiene più di un parser.</span><span class="sxs-lookup"><span data-stu-id="41358-122">However, Network Monitor allows you to create a DLL that contains more than one parser.</span></span> <span data-ttu-id="41358-123">Ad esempio, tcpip.dll è un Network Monitor DLL con più di un parser.</span><span class="sxs-lookup"><span data-stu-id="41358-123">For example, tcpip.dll is a Network Monitor DLL with more than one parser.</span></span>



| <span data-ttu-id="41358-124">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="41358-124">For information on</span></span>                                               | <span data-ttu-id="41358-125">Vedere</span><span class="sxs-lookup"><span data-stu-id="41358-125">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="41358-126">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="41358-126">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="41358-127">Parser</span><span class="sxs-lookup"><span data-stu-id="41358-127">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="41358-128">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="41358-128">Which entry points are included in the parser DLL.</span></span>               | [<span data-ttu-id="41358-129">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="41358-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="41358-130">L'implementazione di **ParserAutoInstallInfo**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="41358-130">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="41358-131">Implementazione di ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="41358-131">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="41358-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41358-132">Requirements</span></span>



| <span data-ttu-id="41358-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="41358-133">Requirement</span></span> | <span data-ttu-id="41358-134">Valore</span><span class="sxs-lookup"><span data-stu-id="41358-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41358-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41358-135">Minimum supported client</span></span><br/> | <span data-ttu-id="41358-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41358-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41358-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41358-137">Minimum supported server</span></span><br/> | <span data-ttu-id="41358-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41358-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41358-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41358-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="41358-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41358-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41358-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41358-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41358-142">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="41358-142">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




