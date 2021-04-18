---
description: Il messaggio della linea TAPI \_ APPNEWCALL viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato spontaneamente per suo conto.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Messaggio di LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331035"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="f0cd9-103">\_Messaggio linea APPNEWCALL</span><span class="sxs-lookup"><span data-stu-id="f0cd9-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="f0cd9-104">Il messaggio della **linea TAPI \_ APPNEWCALL** viene inviato per informare un'applicazione quando un nuovo handle di chiamata è stato creato spontaneamente per suo conto (ad eccezione di una chiamata API dall'applicazione, nel qual caso l'handle verrebbe restituito tramite un parametro puntatore passato nella funzione).</span><span class="sxs-lookup"><span data-stu-id="f0cd9-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="f0cd9-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0cd9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0cd9-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f0cd9-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cd9-107">Handle dell'applicazione per il dispositivo della linea in cui è stata creata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="f0cd9-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f0cd9-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cd9-109">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="f0cd9-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f0cd9-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cd9-111">Identificatore dell'indirizzo sulla riga in cui viene visualizzata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="f0cd9-112">Un identificatore di indirizzo è associato in modo permanente a un indirizzo. l'identificatore rimane costante tra gli aggiornamenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="f0cd9-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f0cd9-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cd9-114">Handle dell'applicazione per la nuova chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="f0cd9-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f0cd9-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cd9-116">Il privilegio delle applicazioni per la nuova chiamata (LINECALLPRIVILEGE \_ owner o LINECALLPRIVILEGE \_ monitor).</span><span class="sxs-lookup"><span data-stu-id="f0cd9-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0cd9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0cd9-117">Return value</span></span>

<span data-ttu-id="f0cd9-118">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0cd9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0cd9-119">Remarks</span></span>

<span data-ttu-id="f0cd9-120">Le applicazioni che supportano la versione 2,0 o successive di TAPI ricevono un messaggio di **riga \_ APPNEWCALL** ogni volta che all'applicazione viene assegnato un handle per una nuova chiamata in modo spontaneo.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="f0cd9-121">Poiché il messaggio include i parametri *hLine* e *dwAddressID* in cui è presente la chiamata, l'applicazione può creare rapidamente un nuovo oggetto chiamata nel contesto corretto.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="f0cd9-122">Il messaggio di **riga \_ APPNEWCALL** è sempre seguito immediatamente da un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che indica lo stato iniziale della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="f0cd9-123">Le applicazioni meno recenti (che hanno negoziato una versione API precedente alla 2,0) vengono inviate solo un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) , come documentato nelle versioni precedenti dell'API.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="f0cd9-124">Tali applicazioni creeranno un nuovo oggetto chiamata al momento della ricezione di un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) con *dwParam3* impostato su un valore diverso da zero e contenente un handle di chiamata attualmente non noto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0cd9-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="f0cd9-125">Gli svantaggi sono che (a) l'applicazione deve chiamare [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per determinare i parametri *hLine* e *dwAddressID* associati alla chiamata; (b) l'applicazione deve analizzare tutti gli handle di chiamata noti per determinare che la chiamata è una nuova chiamata; e (c) è possibile, in determinate condizioni, affinché l'applicazione ritenga che riceva un nuovo handle di chiamata quando in realtà ha appena deallocato l'handle alla chiamata (ad esempio, l'applicazione ha appena deallocato un handle di chiamata, ma un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che fornisce la proprietà dell'applicazione della chiamata a causa di un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) da un'altra applicazione è già presente nella coda di messaggi TAPI dell'applicazione).</span><span class="sxs-lookup"><span data-stu-id="f0cd9-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cd9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0cd9-126">Requirements</span></span>



| <span data-ttu-id="f0cd9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0cd9-127">Requirement</span></span> | <span data-ttu-id="f0cd9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f0cd9-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f0cd9-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f0cd9-129">TAPI version</span></span><br/> | <span data-ttu-id="f0cd9-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f0cd9-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f0cd9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0cd9-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f0cd9-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0cd9-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0cd9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0cd9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0cd9-134">**LINEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="f0cd9-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="f0cd9-135">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="f0cd9-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="f0cd9-136">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="f0cd9-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




