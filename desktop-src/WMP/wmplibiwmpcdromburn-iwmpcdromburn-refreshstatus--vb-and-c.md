---
title: Metodo IWMPCdromBurn refreshStatus
description: Il metodo refreshStatus aggiorna le informazioni sullo stato per la playlist Burn corrente.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- Metodo refreshStatus Windows Media Player
- Metodo refreshStatus Windows Media Player, interfaccia IWMPCdromBurn
- Interfaccia IWMPCdromBurn Windows Media Player, metodo refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329655"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="9abc4-106">Metodo IWMPCdromBurn:: refreshStatus</span><span class="sxs-lookup"><span data-stu-id="9abc4-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="9abc4-107">Il metodo **refreshStatus** aggiorna le informazioni sullo stato per la playlist Burn corrente.</span><span class="sxs-lookup"><span data-stu-id="9abc4-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abc4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9abc4-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="9abc4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9abc4-109">Parameters</span></span>

<span data-ttu-id="9abc4-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9abc4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9abc4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9abc4-111">Return value</span></span>

<span data-ttu-id="9abc4-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9abc4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9abc4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9abc4-113">Remarks</span></span>

<span data-ttu-id="9abc4-114">È consigliabile chiamare questo metodo dopo avere creato o modificato una playlist di masterizzazione prima di leggere le informazioni sullo stato o di masterizzare il CD.</span><span class="sxs-lookup"><span data-stu-id="9abc4-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="9abc4-115">È possibile verificare se è necessario un aggiornamento ottenendo il valore di **burnState** e verificando la presenza di wmpbsRefreshStatusPending.</span><span class="sxs-lookup"><span data-stu-id="9abc4-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="9abc4-116">L'aggiornamento dello stato è un'operazione sincrona.</span><span class="sxs-lookup"><span data-stu-id="9abc4-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="9abc4-117">Ciò significa che un periodo di tempo prolungato può trascorrere prima che questo metodo restituisca se la playlist Burn corrente è di grandi dimensioni e contiene numerose modifiche.</span><span class="sxs-lookup"><span data-stu-id="9abc4-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abc4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9abc4-118">Requirements</span></span>



| <span data-ttu-id="9abc4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abc4-119">Requirement</span></span> | <span data-ttu-id="9abc4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9abc4-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abc4-121">Versione</span><span class="sxs-lookup"><span data-stu-id="9abc4-121">Version</span></span><br/>   | <span data-ttu-id="9abc4-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="9abc4-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="9abc4-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9abc4-123">Namespace</span></span><br/> | <span data-ttu-id="9abc4-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9abc4-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9abc4-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="9abc4-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9abc4-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9abc4-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abc4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9abc4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abc4-128">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9abc4-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9abc4-129">**IWMPCdromBurn. burnState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9abc4-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9abc4-130">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="9abc4-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





