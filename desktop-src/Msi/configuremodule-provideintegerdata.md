---
description: Il metodo ProvideIntegerData dell'oggetto ConfigureModule viene chiamato da Mergemod.dll per recuperare dati Integer dallo strumento client.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Metodo ConfigureModule. ProvideIntegerData (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332621"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="1adb2-103">ConfigureModule. ProvideIntegerData, metodo</span><span class="sxs-lookup"><span data-stu-id="1adb2-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="1adb2-104">Il metodo **ProvideIntegerData** dell' [**oggetto ConfigureModule**](configuremodule-object.md) viene chiamato da Mergemod.dll per recuperare dati Integer dallo strumento client.</span><span class="sxs-lookup"><span data-stu-id="1adb2-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="1adb2-105">Mergemod.dll fornisce il *nome* dalla voce corrispondente nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1adb2-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="1adb2-106">Lo strumento deve restituire S \_ OK e fornire l'intero di personalizzazione appropriato in *ConfigData*.</span><span class="sxs-lookup"><span data-stu-id="1adb2-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="1adb2-107">Se lo strumento non fornisce dati di configurazione per questo valore del *nome* , la funzione deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="1adb2-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="1adb2-108">In questo caso Mergemod.dll ignora il valore dell'argomento *ConfigData* e usa il valore predefinito della tabella ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1adb2-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1adb2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1adb2-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="1adb2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1adb2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1adb2-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="1adb2-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="1adb2-112">Nome dell'elemento per il quale vengono recuperati i dati.</span><span class="sxs-lookup"><span data-stu-id="1adb2-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1adb2-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="1adb2-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="1adb2-114">Puntatore al testo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="1adb2-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1adb2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1adb2-115">Return value</span></span>

<span data-ttu-id="1adb2-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1adb2-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1adb2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1adb2-117">Remarks</span></span>

<span data-ttu-id="1adb2-118">Il client può essere chiamato non più di una volta per ogni record nella [tabella ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1adb2-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="1adb2-119">Si noti che Mergemod.dll non effettua mai più chiamate al client per lo stesso valore "Name".</span><span class="sxs-lookup"><span data-stu-id="1adb2-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="1adb2-120">Se nessun record nella tabella ModuleSubstitution usa la proprietà, una voce nella tabella ModuleConfiguration non comporta chiamate al client.</span><span class="sxs-lookup"><span data-stu-id="1adb2-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="1adb2-121">C++</span><span class="sxs-lookup"><span data-stu-id="1adb2-121">C++</span></span>

<span data-ttu-id="1adb2-122">Vedere [**funzione ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="1adb2-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="1adb2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1adb2-123">Requirements</span></span>



| <span data-ttu-id="1adb2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1adb2-124">Requirement</span></span> | <span data-ttu-id="1adb2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1adb2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1adb2-126">Versione</span><span class="sxs-lookup"><span data-stu-id="1adb2-126">Version</span></span><br/> | <span data-ttu-id="1adb2-127">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1adb2-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1adb2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1adb2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1adb2-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1adb2-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1adb2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1adb2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="1adb2-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adb2-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




