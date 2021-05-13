---
description: Crea un moniker che rappresenta un componente hardware e il gestore eventi associato. AutoPlay usa questa funzione per consentire alle applicazioni di usare gli eventi AutoPlay.
title: Funzione CreateHardwareEventMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841242"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="46bab-104">Funzione CreateHardwareEventMoniker</span><span class="sxs-lookup"><span data-stu-id="46bab-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="46bab-105">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="46bab-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="46bab-106">Potrebbe essere stato modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46bab-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="46bab-107">Crea un moniker che rappresenta un componente hardware e il gestore eventi associato.</span><span class="sxs-lookup"><span data-stu-id="46bab-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="46bab-108">AutoPlay usa questa funzione per consentire alle applicazioni di usare gli eventi AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="46bab-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="46bab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46bab-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="46bab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="46bab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46bab-111">*clsid* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46bab-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46bab-112">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="46bab-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="46bab-113">ID della classe a cui viene associato il moniker.</span><span class="sxs-lookup"><span data-stu-id="46bab-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="46bab-114">*pszEventHandler* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46bab-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46bab-115">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="46bab-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="46bab-116">Nome del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="46bab-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="46bab-117">*ppmoniker* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="46bab-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46bab-118">Tipo: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="46bab-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="46bab-119">Indirizzo di una variabile puntatore che riceve il puntatore a [**interfaccia IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)</span><span class="sxs-lookup"><span data-stu-id="46bab-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46bab-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46bab-120">Return value</span></span>

<span data-ttu-id="46bab-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46bab-121">Type: **HRESULT**</span></span>

<span data-ttu-id="46bab-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46bab-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46bab-123">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="46bab-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46bab-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="46bab-124">Remarks</span></span>

<span data-ttu-id="46bab-125">Usare **CreateHardwareEventMoniker durante** la registrazione delle applicazioni in esecuzione in modo che tali applicazioni hanno accesso agli eventi AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="46bab-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="46bab-126">Per usare gli eventi AutoPlay nelle applicazioni in esecuzione, è innanzitutto necessario creare un nuovo componente che implementa [**l'interfaccia IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)</span><span class="sxs-lookup"><span data-stu-id="46bab-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="46bab-127">Inizializza questa interfaccia con il valore InitCmdLine dalla voce del gestore specifico sotto la chiave **Handlers,** perché AutoPlay non chiama il [**metodo Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize)</span><span class="sxs-lookup"><span data-stu-id="46bab-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="46bab-128">È necessario chiamare **CreateHardwareEventMoniker** per ottenere un moniker che rappresenta il componente e il relativo gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="46bab-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="46bab-129">Usare quindi il valore restituito nel *parametro ppmoniker* per registrare il componente nella tabella degli oggetti in esecuzione (ROT, Running Object Table), come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="46bab-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="46bab-130">Si noti **che CreateHardwareEventMoniker** non è definito in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="46bab-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="46bab-131">Per usarlo nel codice, è necessario ottenere un handle per il file Shsvcs.dll tramite una chiamata a [**LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)</span><span class="sxs-lookup"><span data-stu-id="46bab-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="46bab-132">Usare quindi tale handle in una chiamata a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere un'istanza della **funzione CreateHardwareEventMoniker.**</span><span class="sxs-lookup"><span data-stu-id="46bab-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="46bab-133">La chiamata a [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) richiede l'immissione delle informazioni **AppID** seguenti nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="46bab-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="46bab-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46bab-134">Requirements</span></span>



| <span data-ttu-id="46bab-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="46bab-135">Requirement</span></span> | <span data-ttu-id="46bab-136">Valore</span><span class="sxs-lookup"><span data-stu-id="46bab-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46bab-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46bab-137">Minimum supported client</span></span><br/> | <span data-ttu-id="46bab-138">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="46bab-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="46bab-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46bab-139">Minimum supported server</span></span><br/> | <span data-ttu-id="46bab-140">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46bab-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46bab-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46bab-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="46bab-142"><dt>Nessuna</dt></span><span class="sxs-lookup"><span data-stu-id="46bab-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="46bab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="46bab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46bab-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46bab-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
