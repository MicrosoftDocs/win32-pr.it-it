---
description: Carica la DLL di monitoraggio.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Funzione OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308159"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="5c297-103">OnLoadingDLL (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c297-103">OnLoadingDLL function</span></span>

<span data-ttu-id="5c297-104">La funzione **OnLoadingDLL** carica la dll di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c297-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c297-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="5c297-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c297-107">*hFilterBlob* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5c297-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-108">Un BLOB utilizzato dal MCSVC per trovare la corrispondenza con un monitoraggio con NIC disponibili.</span><span class="sxs-lookup"><span data-stu-id="5c297-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="5c297-109">Questo parametro contiene sempre una richiesta per un'interfaccia [IRTC](irtc.md) , quindi la maggior parte dei monitoraggi non è necessario aggiungere alcuna voce al BLOB.</span><span class="sxs-lookup"><span data-stu-id="5c297-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="5c297-110">Un monitoraggio personalizzato, tuttavia, può aggiungere altri criteri di filtro, ad esempio il tipo MAC deve essere Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5c297-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="5c297-111">*pCreateFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c297-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-112">Flag che indicano il modo in cui MCSVC controlla la creazione di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="5c297-113">Questo parametro deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c297-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="5c297-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5c297-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="5c297-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5c297-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="5c297-116"><dt>**MCS \_ crearne \_ uno \_ per ogni \_ scheda**</dt></span><span class="sxs-lookup"><span data-stu-id="5c297-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="5c297-117">MCSVC garantisce che esista una sola istanza di questo monitoraggio per ogni scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5c297-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="5c297-118">Una seconda istanza può essere creata solo se la prima viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="5c297-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="5c297-119"><dt>**\_ \_ \_ per \_ impostazione predefinita, MCS crea le configurazioni**</dt></span><span class="sxs-lookup"><span data-stu-id="5c297-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="5c297-120">Se il monitoraggio ha una configurazione interna predefinita, MCSVC non richiede all'utente di configurare il monitoraggio prima della creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5c297-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="5c297-121">*ppDefaultName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c297-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-122">Puntatore a un puntatore all'indirizzo del nome predefinito del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="5c297-123">MCSVC utilizza il nome predefinito durante la creazione di istanze del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="5c297-124">Se, ad esempio, il nome predefinito restituito è "Monitoraggio router", la prima istanza di monitoraggio sarà "router monitor 1", il secondo sarà "RouterMonitor2 e così via.</span><span class="sxs-lookup"><span data-stu-id="5c297-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="5c297-125">Se viene restituito **null** , MCSVC usa il nome della dll.</span><span class="sxs-lookup"><span data-stu-id="5c297-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="5c297-126">*ppDescription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c297-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-127">Puntatore a un puntatore all'indirizzo della descrizione del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="5c297-128">La descrizione viene passata allo strumento di controllo del monitoraggio, che utilizza la descrizione per indicare all'utente che il monitoraggio esiste.</span><span class="sxs-lookup"><span data-stu-id="5c297-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="5c297-129">Questo parametro può restituire **null**.</span><span class="sxs-lookup"><span data-stu-id="5c297-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5c297-130">*ppDefaultScript* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c297-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-131">Puntatore a un puntatore all'indirizzo dello script del modulo HTML predefinito utilizzato per configurare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="5c297-132">Sebbene le istanze del monitoraggio possano modificare il proprio script, la maggior parte dei monitoraggi caricano semplicemente lo script una sola volta, da un file.</span><span class="sxs-lookup"><span data-stu-id="5c297-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="5c297-133">Il valore di *ppDefaultScript* può essere **null**. Tuttavia, il monitoraggio non può essere configurato esternamente o deve fornire uno script in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="5c297-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="5c297-134">È più efficiente fornire uno script predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c297-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="5c297-135">*ppDefaultConfig* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c297-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c297-136">Indirizzo della stringa predefinita utilizzata per configurare il monitoraggio quando viene creato.</span><span class="sxs-lookup"><span data-stu-id="5c297-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="5c297-137">Questo parametro può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="5c297-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c297-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c297-138">Return value</span></span>

<span data-ttu-id="5c297-139">Se la funzione ha esito positivo, il valore restituito è S \_ OK, che corrisponde a NOERROR.</span><span class="sxs-lookup"><span data-stu-id="5c297-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="5c297-140">Se la funzione ha esito negativo, MCSVC omette il monitor specificato da tutti i relativi elenchi; in seguito, non è possibile creare alcun monitoraggio di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="5c297-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c297-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c297-141">Remarks</span></span>

<span data-ttu-id="5c297-142">La funzione **OnLoadingDLL** viene chiamata una volta da MCSVC, quando carica la dll per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="5c297-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="5c297-143">La DLL fornisce quindi i valori predefiniti che verranno usati da MCSVC durante la creazione di un'istanza di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5c297-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="5c297-144">Il monitoraggio deve allocare tutta la memoria necessaria per le stringhe restituite a MCSVC.</span><span class="sxs-lookup"><span data-stu-id="5c297-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="5c297-145">Quando viene restituito, MCSVC crea copie di tutte le stringhe e non tenta di liberare le stringhe restituite.</span><span class="sxs-lookup"><span data-stu-id="5c297-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="5c297-146">Il monitoraggio deve usare funzioni helper BLOB per modificare il BLOB del filtro.</span><span class="sxs-lookup"><span data-stu-id="5c297-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c297-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c297-147">Requirements</span></span>



| <span data-ttu-id="5c297-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c297-148">Requirement</span></span> | <span data-ttu-id="5c297-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5c297-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c297-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c297-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5c297-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c297-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c297-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c297-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5c297-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c297-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c297-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c297-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c297-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c297-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




