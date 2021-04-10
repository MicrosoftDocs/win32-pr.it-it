---
description: La funzione DllGetMonitorObject deve essere implementata dal monitoraggio. MCSVC chiama questa funzione per creare un'istanza del monitoraggio.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Funzione di callback DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884866"
---
# <a name="dllgetmonitorobject-callback-function"></a><span data-ttu-id="015de-104">Funzione di callback DllGetMonitorObject</span><span class="sxs-lookup"><span data-stu-id="015de-104">DllGetMonitorObject callback function</span></span>

<span data-ttu-id="015de-105">La funzione **DllGetMonitorObject** deve essere implementata dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="015de-105">The **DllGetMonitorObject** function must be implemented by the monitor.</span></span> <span data-ttu-id="015de-106">MCSVC chiama questa funzione per creare un'istanza del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="015de-106">The MCSVC calls this function to create an instance of the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="015de-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="015de-107">Syntax</span></span>


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="015de-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="015de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="015de-109">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="015de-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="015de-110">UUID dei monitoraggi, illustrato di seguito, come definito nel file di intestazione IMonitor. h.</span><span class="sxs-lookup"><span data-stu-id="015de-110">UUID of monitors, shown below, as defined in the IMonitor.h header file.</span></span> <span data-ttu-id="015de-111">Se viene fornito un UUID non valido, la funzione ha esito negativo e il monitoraggio deve restituire E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="015de-111">If an invalid UUID is provided, the function fails, and the monitor must return E\_NOINTERFACE.</span></span>

``` syntax
IID_IMonitor
```

</dd> <dt>

<span data-ttu-id="015de-112">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="015de-112">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="015de-113">Puntatore a un puntatore che riceve l'interfaccia richiesta in *riid*.</span><span class="sxs-lookup"><span data-stu-id="015de-113">Pointer to a pointer that receives the interface requested in *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="015de-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="015de-114">Return value</span></span>

<span data-ttu-id="015de-115">Se la funzione ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).</span><span class="sxs-lookup"><span data-stu-id="015de-115">If the function is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="015de-116">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="015de-116">If the function is unsuccessful, the return value is a failure code.</span></span> <span data-ttu-id="015de-117">Quando viene restituito un codice di errore, MCSVC non crea l'oggetto di monitoraggio e il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) non viene chiamato sul puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="015de-117">When a failure code is returned, the MCSVC does not create the monitor object, and the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method is not called on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="015de-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="015de-118">Remarks</span></span>

<span data-ttu-id="015de-119">La funzione **DllGetMonitorObject** viene chiamata ogni volta che il MCSVC tenta di creare un'istanza del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="015de-119">The **DllGetMonitorObject** function is called each time the MCSVC tries to create an instance of the monitor.</span></span> <span data-ttu-id="015de-120">Questa funzione presenta intenzionalmente una forte somiglianza con la funzione [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) più comune.</span><span class="sxs-lookup"><span data-stu-id="015de-120">This function intentionally bears a strong resemblance to the more common [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) function.</span></span> <span data-ttu-id="015de-121">La differenza principale consiste nel fatto che un CLSID non viene passato a **DllGetMonitorObject**.</span><span class="sxs-lookup"><span data-stu-id="015de-121">The main difference is that a CLSID is not passed in to **DllGetMonitorObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="015de-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="015de-122">Requirements</span></span>



| <span data-ttu-id="015de-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="015de-123">Requirement</span></span> | <span data-ttu-id="015de-124">Valore</span><span class="sxs-lookup"><span data-stu-id="015de-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="015de-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="015de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="015de-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="015de-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="015de-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="015de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="015de-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="015de-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="015de-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="015de-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="015de-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="015de-130"><dt>Netmon.h</dt></span></span> </dl> |



 

