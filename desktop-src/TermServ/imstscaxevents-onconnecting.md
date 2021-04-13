---
title: Metodo OnConnection IMsTscAxEvents
description: Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Metodo OnConnection Servizi Desktop remoto
- Servizi Desktop remoto del metodo OnConnection, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnConnection
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400232"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="e13fe-106">Metodo IMsTscAxEvents:: OnConnection</span><span class="sxs-lookup"><span data-stu-id="e13fe-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="e13fe-107">Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a [**IMsTscAx:: Connect**](imstscax-connect.md).</span><span class="sxs-lookup"><span data-stu-id="e13fe-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e13fe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e13fe-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="e13fe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e13fe-109">Parameters</span></span>

<span data-ttu-id="e13fe-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e13fe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e13fe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e13fe-111">Return value</span></span>

<span data-ttu-id="e13fe-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e13fe-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13fe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e13fe-113">Remarks</span></span>

<span data-ttu-id="e13fe-114">Implementare questo metodo nel sink di evento per ricevere la notifica che il controllo ha iniziato la connessione.</span><span class="sxs-lookup"><span data-stu-id="e13fe-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="e13fe-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="e13fe-115">Examples</span></span>

<span data-ttu-id="e13fe-116">Nell'esempio seguente viene illustrato come gestire questo evento con Visual Basic codice di scripting.</span><span class="sxs-lookup"><span data-stu-id="e13fe-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="e13fe-117">Il presupposto in questo esempio è che l'oggetto controllo è denominato "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="e13fe-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="e13fe-118">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e13fe-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="e13fe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e13fe-119">Requirements</span></span>



| <span data-ttu-id="e13fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e13fe-120">Requirement</span></span> | <span data-ttu-id="e13fe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e13fe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e13fe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e13fe-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e13fe-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e13fe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e13fe-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e13fe-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e13fe-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e13fe-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="e13fe-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13fe-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e13fe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e13fe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e13fe-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13fe-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e13fe-130">IID</span><span class="sxs-lookup"><span data-stu-id="e13fe-130">IID</span></span><br/>                      | <span data-ttu-id="e13fe-131">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e13fe-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e13fe-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e13fe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13fe-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e13fe-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





