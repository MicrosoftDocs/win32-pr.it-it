---
description: Il metodo SetDynamicReconnectLevel imposta il livello di riconnessione dinamica durante il rendering.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Metodo IRenderEngine:: SetDynamicReconnectLevel (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330790"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="aae28-103">Metodo IRenderEngine:: SetDynamicReconnectLevel</span><span class="sxs-lookup"><span data-stu-id="aae28-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="aae28-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="aae28-104">\[Deprecated.</span></span> <span data-ttu-id="aae28-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aae28-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aae28-106">Il `SetDynamicReconnectLevel` metodo imposta il livello di riconnessione dinamica durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="aae28-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae28-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aae28-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="aae28-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aae28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae28-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="aae28-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="aae28-110">Combinazione di [**flag di riconnessione dinamici**](dynamic-reconnection-flags.md), che specificano il livello di riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="aae28-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae28-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aae28-111">Return value</span></span>

<span data-ttu-id="aae28-112">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="aae28-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="aae28-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="aae28-113">Return code</span></span>                                                                               | <span data-ttu-id="aae28-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aae28-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="aae28-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aae28-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="aae28-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="aae28-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="aae28-117"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="aae28-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="aae28-118">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="aae28-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aae28-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="aae28-119">Remarks</span></span>

<span data-ttu-id="aae28-120">Per impostazione predefinita, il motore di rendering di base carica ogni origine prima di eseguire il rendering di un progetto.</span><span class="sxs-lookup"><span data-stu-id="aae28-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="aae28-121">Questo può comportare un lungo periodo di avvio.</span><span class="sxs-lookup"><span data-stu-id="aae28-121">This can result in a long start-up time.</span></span> <span data-ttu-id="aae28-122">Con la riconnessione dinamica, le origini vengono caricate solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="aae28-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="aae28-123">Questo può ridurre il tempo di avvio, ma potrebbe interferire con la riproduzione uniforme.</span><span class="sxs-lookup"><span data-stu-id="aae28-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="aae28-124">In genere, maggiore è il numero di clip di origine utilizzate da un progetto, più si può trarre vantaggio dalla riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="aae28-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="aae28-125">Il motore di rendering intelligente non implementa questo metodo.</span><span class="sxs-lookup"><span data-stu-id="aae28-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="aae28-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="aae28-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aae28-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aae28-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aae28-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aae28-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aae28-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aae28-129">Requirements</span></span>



| <span data-ttu-id="aae28-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae28-130">Requirement</span></span> | <span data-ttu-id="aae28-131">Valore</span><span class="sxs-lookup"><span data-stu-id="aae28-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aae28-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aae28-132">Header</span></span><br/>  | <dl> <span data-ttu-id="aae28-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae28-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aae28-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="aae28-134">Library</span></span><br/> | <dl> <span data-ttu-id="aae28-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aae28-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae28-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aae28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae28-137">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="aae28-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="aae28-138">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="aae28-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




