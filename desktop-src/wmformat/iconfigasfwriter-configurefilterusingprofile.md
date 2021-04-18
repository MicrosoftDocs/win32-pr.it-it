---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfile
description: Il metodo ConfigureFilterUsingProfile è la modalità consigliata per impostare un profilo. Configura il filtro per scrivere un file ASF basato sul profilo definito dall'applicazione specificato.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Metodo ConfigureFilterUsingProfile Windows Media Format
- Metodo ConfigureFilterUsingProfile Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300277"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="032af-107">Metodo IConfigAsfWriter:: ConfigureFilterUsingProfile</span><span class="sxs-lookup"><span data-stu-id="032af-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="032af-108">Il metodo **ConfigureFilterUsingProfile** è la modalità consigliata per impostare un profilo.</span><span class="sxs-lookup"><span data-stu-id="032af-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="032af-109">Configura il filtro per scrivere un file ASF basato sul profilo definito dall'applicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="032af-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="032af-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="032af-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="032af-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="032af-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032af-112">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="032af-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="032af-113">Puntatore all'interfaccia [**IWMProfile**](iwmprofile.md) nel profilo definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="032af-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032af-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="032af-114">Return value</span></span>

<span data-ttu-id="032af-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="032af-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="032af-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="032af-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="032af-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="032af-117">Return code</span></span>                                                                                         | <span data-ttu-id="032af-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="032af-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="032af-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="032af-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="032af-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="032af-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="032af-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="032af-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="032af-122">Puntatore all'interfaccia **IWMProfile** non valido.</span><span class="sxs-lookup"><span data-stu-id="032af-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="032af-123"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="032af-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="032af-124">Il grafico è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="032af-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="032af-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="032af-125">Remarks</span></span>

<span data-ttu-id="032af-126">Se ha esito positivo, questo metodo provocherà l'invio di un evento di **\_ \_ modifica del grafo EC** all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="032af-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="032af-127">Utilizzare questo metodo per configurare il writer con un profilo della serie Windows Media 9 personalizzato creato (o caricato da un file con estensione prx esistente) utilizzando i metodi di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="032af-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="032af-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="032af-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="032af-129">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="032af-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

