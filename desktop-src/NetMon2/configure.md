---
description: Configura l'esperto nella DLL di esperti.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configura funzione di callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311630"
---
# <a name="configure-callback-function"></a><span data-ttu-id="23c27-103">Configura funzione di callback</span><span class="sxs-lookup"><span data-stu-id="23c27-103">Configure callback function</span></span>

<span data-ttu-id="23c27-104">La funzione **Configure** configura l'esperto nella dll Expert.</span><span class="sxs-lookup"><span data-stu-id="23c27-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="23c27-105">L'esperto deve implementare la funzione **Configure** .</span><span class="sxs-lookup"><span data-stu-id="23c27-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="23c27-106">Quando viene ricevuta la chiamata di funzione, l'esperto Visualizza una finestra di dialogo che consente all'utente di modificare qualsiasi elemento configurabile.</span><span class="sxs-lookup"><span data-stu-id="23c27-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c27-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23c27-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="23c27-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23c27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c27-109">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23c27-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c27-110">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="23c27-110">Unique expert identifier.</span></span>

<span data-ttu-id="23c27-111">L'identificatore univoco viene passato di nuovo a tutte le funzioni di Network Monitor specifiche dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="23c27-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="23c27-112">Tenere presente che l'identificatore non può essere la stessa chiave esperta di quella passata alla funzione [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="23c27-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="23c27-113">Non archiviare la chiave Expert dalla chiamata **Configure** .</span><span class="sxs-lookup"><span data-stu-id="23c27-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="23c27-114">*ppConfig* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="23c27-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="23c27-115">Puntatore a un puntatore a una struttura [**EXPERTCONFIG**](expertconfig.md) alla voce.</span><span class="sxs-lookup"><span data-stu-id="23c27-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="23c27-116">Dopo una corretta uscita, la struttura [**EXPERTCONFIG**](expertconfig.md) a cui si fa riferimento contiene i nuovi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="23c27-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="23c27-117">*pExpertStartupInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23c27-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c27-118">Puntatore all'elemento Capture con lo stato attivo all'avvio dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="23c27-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="23c27-119">*StartupFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23c27-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c27-120">Flag che indicano il modo in cui l'esperto deve utilizzare il parametro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="23c27-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="23c27-121">L'unico flag definito è **\_ flag di avvio esperto usare i dati di \_ \_ \_ avvio \_ \_ sui \_ \_ dati di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="23c27-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="23c27-122">Il flag indica che l'esperto utilizzerà il parametro *pExpertStartupInfo* anziché il parametro *ppConfig* passato.</span><span class="sxs-lookup"><span data-stu-id="23c27-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="23c27-123">In genere, il flag viene impostato quando si avvia l'esperto da un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="23c27-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="23c27-124">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23c27-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c27-125">Handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="23c27-125">A handle to the parent window.</span></span> <span data-ttu-id="23c27-126">Utilizzare l'handle per aprire una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="23c27-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c27-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23c27-127">Return value</span></span>

<span data-ttu-id="23c27-128">Se la funzione ha esito positivo, ovvero se è presente una configurazione corrente, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="23c27-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="23c27-129">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="23c27-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c27-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="23c27-130">Remarks</span></span>

<span data-ttu-id="23c27-131">Network Monitor chiama la funzione **Configure** con la configurazione corrente dell'esperto, se ne esiste una.</span><span class="sxs-lookup"><span data-stu-id="23c27-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="23c27-132">L'esperto Visualizza una finestra di dialogo con cui è possibile modificare qualsiasi elemento configurabile.</span><span class="sxs-lookup"><span data-stu-id="23c27-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="23c27-133">Quando *ppConfig* viene passato in e Network Monitor non dispone di una configurazione archiviata per l'esperto specificato, il valore del parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="23c27-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="23c27-134">In questo caso, per aprire la finestra di dialogo la funzione **Configure** presuppone i valori predefiniti hardcoded (oppure usa le informazioni di avvio).</span><span class="sxs-lookup"><span data-stu-id="23c27-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="23c27-135">I dati di configurazione possono anche essere **null** quando la funzione **Configure** restituisce e viene passato un **valore null** .</span><span class="sxs-lookup"><span data-stu-id="23c27-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="23c27-136">Questa situazione si verifica quando Network Monitor non dispone di un valore predefinito archiviato e l'utente preme **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="23c27-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="23c27-137">L'inizio della struttura di dati [**EXPERTCONFIG**](expertconfig.md) include una sezione privata che archivia le informazioni sulle dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="23c27-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="23c27-138">La dimensione della struttura **EXPERTCONFIG** deve includere la lunghezza **DWORD** riservata visualizzata all'inizio della struttura.</span><span class="sxs-lookup"><span data-stu-id="23c27-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="23c27-139">Se, ad esempio, i dati di configurazione richiedono 20 byte di spazio di archiviazione, allocare 24 byte per archiviare i dati.</span><span class="sxs-lookup"><span data-stu-id="23c27-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="23c27-140">Se *ppConfig* è **null**, la funzione **Configure** chiama la funzione [**ExpertAllocMemory**](expertallocmemory.md) per allocare una nuova configurazione con le dimensioni corrette.</span><span class="sxs-lookup"><span data-stu-id="23c27-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="23c27-141">Se il buffer non è sufficiente per conservare i dati esperti, l'esperto deve chiamare la funzione [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="23c27-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="23c27-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23c27-142">Requirements</span></span>



| <span data-ttu-id="23c27-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c27-143">Requirement</span></span> | <span data-ttu-id="23c27-144">Valore</span><span class="sxs-lookup"><span data-stu-id="23c27-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23c27-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23c27-145">Minimum supported client</span></span><br/> | <span data-ttu-id="23c27-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23c27-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="23c27-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23c27-147">Minimum supported server</span></span><br/> | <span data-ttu-id="23c27-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23c27-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="23c27-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23c27-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c27-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c27-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




