---
description: Stima il rischio di esecuzione di codice sconosciuto quando un gestore viene chiamato su un determinato file. Questo rischio si basa su una conoscenza del gestore e del contenuto del codice del file.
title: Funzione EstimateFileRiskLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841432"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="91e22-104">Funzione EstimateFileRiskLevel</span><span class="sxs-lookup"><span data-stu-id="91e22-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="91e22-105">\[Questa funzione è disponibile in Windows XP con Service Pack 2 (SP2) tramite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="91e22-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="91e22-106">Potrebbe essere stato modificato o non disponibile nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="91e22-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="91e22-107">Le applicazioni client devono invece usare [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) per presentare un ambiente utente che fornisce download e scambio sicuri di file tramite allegati di posta elettronica e messaggistica.\]</span><span class="sxs-lookup"><span data-stu-id="91e22-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="91e22-108">Stima il rischio di esecuzione di codice sconosciuto quando un gestore viene chiamato su un determinato file.</span><span class="sxs-lookup"><span data-stu-id="91e22-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="91e22-109">Questo rischio si basa su una conoscenza del gestore e del contenuto del codice del file.</span><span class="sxs-lookup"><span data-stu-id="91e22-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e22-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91e22-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="91e22-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="91e22-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e22-112">*pszFilePath* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91e22-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e22-113">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="91e22-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="91e22-114">Puntatore a una stringa con terminazione Null che contiene il percorso del file sottoposto a controllo rispetto al gestore.</span><span class="sxs-lookup"><span data-stu-id="91e22-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="91e22-115">*pszExt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91e22-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e22-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="91e22-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="91e22-117">Puntatore a una stringa con terminazione Null che contiene l'estensione del file da controllare, con o senza il relativo punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="91e22-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="91e22-118">Ad esempio, ".txt" o "txt".</span><span class="sxs-lookup"><span data-stu-id="91e22-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="91e22-119">*pszHandler* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91e22-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e22-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="91e22-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="91e22-121">Puntatore a una stringa con terminazione Null che contiene il percorso del gestore per il file.</span><span class="sxs-lookup"><span data-stu-id="91e22-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="91e22-122">*pfrlEstimate* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="91e22-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91e22-123">Tipo: **LIVELLO DI RISCHIO \_ \_ FILE \***</span><span class="sxs-lookup"><span data-stu-id="91e22-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="91e22-124">Quando questa funzione viene restituita correttamente, contiene un puntatore a uno dei valori seguenti che indica il rischio stimato.</span><span class="sxs-lookup"><span data-stu-id="91e22-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="91e22-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ NO \_ OPINION** (0)</span><span class="sxs-lookup"><span data-stu-id="91e22-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="91e22-126">Il formato del file non è identificato o il gestore non è identificato.</span><span class="sxs-lookup"><span data-stu-id="91e22-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="91e22-127">Informazioni insufficienti disponibili per una risposta significativa.</span><span class="sxs-lookup"><span data-stu-id="91e22-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="91e22-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ LOW** (1)</span><span class="sxs-lookup"><span data-stu-id="91e22-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="91e22-129">Il formato del file è completamente comprensibile, il gestore è noto ed è molto sicuro che non verrà eseguito codice estraneo.</span><span class="sxs-lookup"><span data-stu-id="91e22-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="91e22-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODERATE** (2)</span><span class="sxs-lookup"><span data-stu-id="91e22-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91e22-131">Il formato del file è identificato, ma non è sufficientemente comprensibile da etichettare come un rischio elevato o basso.</span><span class="sxs-lookup"><span data-stu-id="91e22-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="91e22-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ HIGH** (3)</span><span class="sxs-lookup"><span data-stu-id="91e22-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91e22-133">Il formato del file viene riconosciuto e sono stati identificati fattori di rischio elevati.</span><span class="sxs-lookup"><span data-stu-id="91e22-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="91e22-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOCK** (4)</span><span class="sxs-lookup"><span data-stu-id="91e22-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91e22-135">Il formato di file è bloccato in modo specifico per questo gestore.</span><span class="sxs-lookup"><span data-stu-id="91e22-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e22-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91e22-136">Return value</span></span>

<span data-ttu-id="91e22-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="91e22-137">Type: **HRESULT**</span></span>

<span data-ttu-id="91e22-138">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="91e22-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91e22-139">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="91e22-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e22-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="91e22-140">Remarks</span></span>

<span data-ttu-id="91e22-141">Questa funzione non è dichiarata in un'intestazione pubblica o inclusa in un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="91e22-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="91e22-142">Per usarlo, è necessario caricarlo direttamente dal Winshfhc.dll ordinale 101.</span><span class="sxs-lookup"><span data-stu-id="91e22-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="91e22-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91e22-143">Requirements</span></span>



| <span data-ttu-id="91e22-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e22-144">Requirement</span></span> | <span data-ttu-id="91e22-145">Valore</span><span class="sxs-lookup"><span data-stu-id="91e22-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e22-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91e22-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91e22-147">Solo Windows XP con app desktop SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="91e22-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91e22-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91e22-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91e22-149">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91e22-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91e22-150">DLL</span><span class="sxs-lookup"><span data-stu-id="91e22-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91e22-151"><dt>Winshfhc.dll (versione 5.1 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="91e22-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




