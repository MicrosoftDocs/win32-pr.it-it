---
description: Il \_ metodo get Owner Recupera il proprietario della finestra corrente.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Metodo CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328356"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="01b45-103">Metodo CBaseControlWindow. Get \_ Owner</span><span class="sxs-lookup"><span data-stu-id="01b45-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="01b45-104">Il `get_Owner` metodo recupera il proprietario della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="01b45-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01b45-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="01b45-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01b45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01b45-107">*Proprietario*</span><span class="sxs-lookup"><span data-stu-id="01b45-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="01b45-108">Puntatore al proprietario della finestra.</span><span class="sxs-lookup"><span data-stu-id="01b45-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01b45-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01b45-109">Return value</span></span>

<span data-ttu-id="01b45-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01b45-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b45-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="01b45-111">Remarks</span></span>

<span data-ttu-id="01b45-112">La finestra video può rientrare in un ambiente di documento.</span><span class="sxs-lookup"><span data-stu-id="01b45-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="01b45-113">A tale scopo, è necessario che la finestra sia costituita da un elemento figlio di un'altra finestra, in modo che venga ritagliata e spostata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="01b45-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="01b45-114">Questa proprietà consente di impostare e recuperare il proprietario della finestra.</span><span class="sxs-lookup"><span data-stu-id="01b45-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="01b45-115">Quando la finestra è di proprietà di un'altra finestra, viene semplicemente chiamata la funzione **padre** di Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="01b45-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="01b45-116">Un'applicazione che chiama questa funzione modificherà gli stili della finestra in modo da impostare il \_ bit WS figlio su.</span><span class="sxs-lookup"><span data-stu-id="01b45-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="01b45-117">Quando la finestra è di proprietà di un'altra finestra, verranno automaticamente trasmessi determinati set di messaggi (in particolare, i messaggi del mouse e della tastiera).</span><span class="sxs-lookup"><span data-stu-id="01b45-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="01b45-118">Questo consente a un'applicazione di eseguire semplici modifiche e altre interazioni.</span><span class="sxs-lookup"><span data-stu-id="01b45-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="01b45-119">Questa funzione membro deve essere chiamata da oggetti esterni tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato.</span><span class="sxs-lookup"><span data-stu-id="01b45-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="01b45-120">Chiamare la funzione membro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) per recuperare questa proprietà se non viene chiamata da un oggetto esterno.</span><span class="sxs-lookup"><span data-stu-id="01b45-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b45-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b45-121">Requirements</span></span>



| <span data-ttu-id="01b45-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b45-122">Requirement</span></span> | <span data-ttu-id="01b45-123">Valore</span><span class="sxs-lookup"><span data-stu-id="01b45-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b45-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01b45-124">Header</span></span><br/>  | <dl> <span data-ttu-id="01b45-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01b45-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01b45-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="01b45-126">Library</span></span><br/> | <dl> <span data-ttu-id="01b45-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01b45-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01b45-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01b45-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01b45-129">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="01b45-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




