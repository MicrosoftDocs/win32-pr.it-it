---
title: Evento ConnectionStatusChanged
description: Si verifica quando cambia lo stato della connessione di rete del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API di streaming multimediale per gli eventi ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726762"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="2e1ce-104">Evento ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="2e1ce-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="2e1ce-105">Si verifica quando cambia lo stato della connessione di rete del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1ce-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e1ce-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="2e1ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e1ce-107">Parameters</span></span>

<span data-ttu-id="2e1ce-108">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e1ce-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e1ce-109">Return value</span></span>

<span data-ttu-id="2e1ce-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e1ce-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e1ce-111">Remarks</span></span>

<span data-ttu-id="2e1ce-112">Per gestire le notifiche da questo evento, registrare una funzione del gestore eventi [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) usando il metodo [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1ce-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="2e1ce-113">Per annullare la registrazione del gestore eventi, usare il metodo [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1ce-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 