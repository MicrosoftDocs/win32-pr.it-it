---
description: Il \_ metodo Put Owner imposta la finestra padre della finestra video; la finestra padre quindi invia alcuni messaggi alla finestra del video.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Metodo CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331940"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="63846-103">Metodo CBaseControlWindow. put \_ Owner</span><span class="sxs-lookup"><span data-stu-id="63846-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="63846-104">Il `put_Owner` metodo imposta la finestra padre della finestra video; la finestra padre quindi invia alcuni messaggi alla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="63846-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="63846-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63846-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="63846-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63846-107">*Proprietario*</span><span class="sxs-lookup"><span data-stu-id="63846-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="63846-108">Handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="63846-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63846-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63846-109">Return value</span></span>

<span data-ttu-id="63846-110">Restituisce NOERROR.</span><span class="sxs-lookup"><span data-stu-id="63846-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="63846-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="63846-111">Remarks</span></span>

<span data-ttu-id="63846-112">Internamente, questo metodo chiama la funzione **padre** di Microsoft Win32 per impostare il nuovo proprietario e imposta lo stile della finestra padre su WS \_ child.</span><span class="sxs-lookup"><span data-stu-id="63846-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="63846-113">La finestra padre inoltrerà quindi determinati set di messaggi (in particolare, i messaggi del mouse e della tastiera) alla finestra del video.</span><span class="sxs-lookup"><span data-stu-id="63846-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="63846-114">Dopo aver impostato il proprietario della finestra video, è necessario impostare il proprietario su **null** e lo stile della finestra del proprietario su WS \_ OVERLAPPED e WS \_ CLIPCHILDREN prima di rilasciare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="63846-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="63846-115">Quando si imposta il proprietario su **null**, questo metodo disattiva il bit figlio WS della finestra padre \_ .</span><span class="sxs-lookup"><span data-stu-id="63846-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="63846-116">Se il proprietario non viene impostato su **null**, la finestra padre continuerà a passare i messaggi alla finestra video ed è probabile che si verifichino errori durante la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63846-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="63846-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63846-117">Requirements</span></span>



| <span data-ttu-id="63846-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="63846-118">Requirement</span></span> | <span data-ttu-id="63846-119">Valore</span><span class="sxs-lookup"><span data-stu-id="63846-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63846-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63846-120">Header</span></span><br/>  | <dl> <span data-ttu-id="63846-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63846-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63846-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="63846-122">Library</span></span><br/> | <dl> <span data-ttu-id="63846-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63846-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63846-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63846-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63846-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="63846-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




