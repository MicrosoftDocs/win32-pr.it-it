---
description: L'esperto deve implementare la funzione Run. Network Monitor chiama la funzione Run per avviare l'esperto nella DLL Expert.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Funzione di callback Run (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879542"
---
# <a name="run-callback-function"></a><span data-ttu-id="fe8bb-104">Funzione di callback Run</span><span class="sxs-lookup"><span data-stu-id="fe8bb-104">Run callback function</span></span>

<span data-ttu-id="fe8bb-105">L'esperto deve implementare la funzione **Run** .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="fe8bb-106">Network Monitor chiama la funzione **Run** per avviare l'esperto nella dll Expert.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe8bb-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="fe8bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe8bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8bb-109">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-110">Identificatore univoco dell'esperto che viene passato di nuovo a tutte le funzioni di Network Monitor specifiche dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="fe8bb-111">L'identificatore *hExpertKey* può passare una chiave esperta diversa dalla chiave Expert passata dalla funzione [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe8bb-112">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-113">Puntatore alla configurazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="fe8bb-114">Il parametro *pConfig* può essere **null** , che significa che l'esperto può essere eseguito con valori predefiniti hardcoded o informazioni di avvio a cui fa riferimento il parametro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="fe8bb-115">*pExpertStartupInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-116">Puntatore all'elemento Capture che ha lo stato attivo all'avvio dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="fe8bb-117">*StartupFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-118">Indicatore del modo in cui l'esperto deve utilizzare il parametro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="fe8bb-119">L'unico flag definito è:</span><span class="sxs-lookup"><span data-stu-id="fe8bb-119">The only flag defined is:</span></span>



| <span data-ttu-id="fe8bb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8bb-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="fe8bb-121">Significato</span><span class="sxs-lookup"><span data-stu-id="fe8bb-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="fe8bb-122"><dt>**\_flag di avvio esperto usare i dati di \_ \_ \_ avvio \_ \_ sui dati di \_ configurazione \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="fe8bb-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="fe8bb-123">Questo flag indica che l'esperto usa il parametro *pExpertStartupInfo* e non usa il parametro *pConfig* .</span><span class="sxs-lookup"><span data-stu-id="fe8bb-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="fe8bb-124">In genere, è possibile impostare questo flag quando l'esperto può iniziare con un clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="fe8bb-125">Se il flag non è impostato, possono verificarsi le due operazioni seguenti: l'esperto non inizia con un clic con il pulsante destro del mouse oppure l'esperto inizia con un clic con il pulsante destro del mouse e quindi l'utente lo configura.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fe8bb-126">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8bb-127">Il parametro *HWND* dell'elemento padre (in genere l'interfaccia utente Network Monitor).</span><span class="sxs-lookup"><span data-stu-id="fe8bb-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8bb-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe8bb-128">Return value</span></span>

<span data-ttu-id="fe8bb-129">Se la funzione ha esito positivo, ovvero se l'esperto inizia, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="fe8bb-130">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8bb-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe8bb-131">Remarks</span></span>

<span data-ttu-id="fe8bb-132">Durante l'esecuzione, l'esperto esegue il ciclo dei frame nel file di acquisizione e genera un report o crea eventi che mostrano problemi.</span><span class="sxs-lookup"><span data-stu-id="fe8bb-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8bb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe8bb-133">Requirements</span></span>



| <span data-ttu-id="fe8bb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8bb-134">Requirement</span></span> | <span data-ttu-id="fe8bb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8bb-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8bb-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8bb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8bb-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe8bb-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8bb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8bb-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe8bb-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe8bb-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe8bb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8bb-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8bb-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




