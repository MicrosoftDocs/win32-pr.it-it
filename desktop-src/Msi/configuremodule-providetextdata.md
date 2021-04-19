---
description: Il metodo ProvideTextData viene chiamato da Mergemod.dll per recuperare i dati di testo dallo strumento client. Mergemod.dll fornisce il nome dalla voce corrispondente nella tabella ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Metodo ConfigureModule. ProvideTextData (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332620"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="58cc6-104">ConfigureModule. ProvideTextData, metodo</span><span class="sxs-lookup"><span data-stu-id="58cc6-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="58cc6-105">Il metodo **ProvideTextData** viene chiamato da Mergemod.dll per recuperare i dati di testo dallo strumento client.</span><span class="sxs-lookup"><span data-stu-id="58cc6-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="58cc6-106">Mergemod.dll fornisce il *nome* dalla voce corrispondente nella tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="58cc6-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="58cc6-107">Lo strumento deve restituire S \_ OK e fornire il testo di personalizzazione appropriato in ConfigData.</span><span class="sxs-lookup"><span data-stu-id="58cc6-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="58cc6-108">Lo strumento client è responsabile dell'allocazione dei dati, ma Mergemod.dllè responsabile del rilascio della memoria.</span><span class="sxs-lookup"><span data-stu-id="58cc6-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="58cc6-109">Questo argomento deve essere un oggetto **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="58cc6-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="58cc6-110">**LPCWSTR** non è accettato.</span><span class="sxs-lookup"><span data-stu-id="58cc6-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="58cc6-111">Se lo strumento non fornisce dati di configurazione per questo valore del *nome* , la funzione deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="58cc6-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="58cc6-112">In questo caso Mergemod.dll ignora il valore dell'argomento ConfigData e usa il valore predefinito della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="58cc6-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="58cc6-113">Il codice restituito diverso da S \_ OK o s \_ false causerà la registrazione di un errore (se un log è aperto) e l'operazione di Unione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="58cc6-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="58cc6-114">Poiché questa funzione segue la convenzione **BSTR** standard, null equivale alla stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="58cc6-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="58cc6-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58cc6-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="58cc6-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="58cc6-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58cc6-117">*Nome*</span><span class="sxs-lookup"><span data-stu-id="58cc6-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="58cc6-118">Nome dell'elemento per il quale vengono recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="58cc6-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="58cc6-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="58cc6-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="58cc6-120">Puntatore al testo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="58cc6-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58cc6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58cc6-121">Return value</span></span>

<span data-ttu-id="58cc6-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="58cc6-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58cc6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="58cc6-123">Remarks</span></span>

<span data-ttu-id="58cc6-124">Il client può essere chiamato non più di una volta per ogni record nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="58cc6-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="58cc6-125">Si noti che Mergemod.dll non effettua mai più chiamate al client per lo stesso valore "Name".</span><span class="sxs-lookup"><span data-stu-id="58cc6-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="58cc6-126">Se nessun record nella tabella ModuleSubstitution usa la proprietà, una voce nella tabella ModuleConfiguration non comporta chiamate al client.</span><span class="sxs-lookup"><span data-stu-id="58cc6-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="58cc6-127">C++</span><span class="sxs-lookup"><span data-stu-id="58cc6-127">C++</span></span>

<span data-ttu-id="58cc6-128">Vedere [**funzione ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="58cc6-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="58cc6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58cc6-129">Requirements</span></span>



| <span data-ttu-id="58cc6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="58cc6-130">Requirement</span></span> | <span data-ttu-id="58cc6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="58cc6-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58cc6-132">Versione</span><span class="sxs-lookup"><span data-stu-id="58cc6-132">Version</span></span><br/> | <span data-ttu-id="58cc6-133">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="58cc6-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="58cc6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58cc6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="58cc6-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="58cc6-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="58cc6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58cc6-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="58cc6-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58cc6-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




