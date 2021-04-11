---
description: Installa un nuovo dispositivo. All'utente viene richiesto di selezionare il dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127290"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="dedc1-104">InstallNewDevice (funzione)</span><span class="sxs-lookup"><span data-stu-id="dedc1-104">InstallNewDevice function</span></span>

<span data-ttu-id="dedc1-105">Installa un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dedc1-105">Installs a new device.</span></span> <span data-ttu-id="dedc1-106">All'utente viene richiesto di selezionare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dedc1-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dedc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dedc1-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="dedc1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dedc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedc1-109">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dedc1-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedc1-110">Handle per la finestra di primo livello da utilizzare per qualsiasi interfaccia utente richiesta.</span><span class="sxs-lookup"><span data-stu-id="dedc1-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="dedc1-111">*ClassGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dedc1-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedc1-112">Puntatore a un **GUID** di classe.</span><span class="sxs-lookup"><span data-stu-id="dedc1-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="dedc1-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dedc1-113">This parameter is optional.</span></span> <span data-ttu-id="dedc1-114">Se questo parametro è **null**, l'utente inizia dalla pagina scelta del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="dedc1-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="dedc1-115">Se questo parametro è **GUID \_ null** o **GUID \_ devclass \_ Unknown**, l'utente inizia dalla pagina di selezione della classe.</span><span class="sxs-lookup"><span data-stu-id="dedc1-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="dedc1-116">*preavvio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dedc1-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dedc1-117">Puntatore a una variabile che riceve lo stato di riavvio.</span><span class="sxs-lookup"><span data-stu-id="dedc1-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="dedc1-118">Questo parametro può essere **di \_ NEEDRESTART** o **di \_ NEEDREBOOT**.</span><span class="sxs-lookup"><span data-stu-id="dedc1-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dedc1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dedc1-119">Return value</span></span>

<span data-ttu-id="dedc1-120">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="dedc1-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="dedc1-121">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="dedc1-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="dedc1-122">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="dedc1-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="dedc1-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dedc1-123">Remarks</span></span>

<span data-ttu-id="dedc1-124">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="dedc1-124">This function has no associated import library.</span></span> <span data-ttu-id="dedc1-125">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a NewDev.dll.</span><span class="sxs-lookup"><span data-stu-id="dedc1-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedc1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dedc1-126">Requirements</span></span>



| <span data-ttu-id="dedc1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedc1-127">Requirement</span></span> | <span data-ttu-id="dedc1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dedc1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dedc1-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dedc1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dedc1-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dedc1-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="dedc1-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dedc1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dedc1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dedc1-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="dedc1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dedc1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dedc1-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dedc1-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedc1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dedc1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedc1-136">Funzioni di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="dedc1-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

