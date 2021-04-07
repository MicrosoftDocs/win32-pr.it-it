---
description: Esegue la registrazione per la notifica quando una DLL viene caricata per la prima volta. Questa notifica si verifica prima che venga eseguito il collegamento dinamico.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049101"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="23eb9-104">LdrRegisterDllNotification (funzione)</span><span class="sxs-lookup"><span data-stu-id="23eb9-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="23eb9-105">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="23eb9-106">Esegue la registrazione per la notifica quando una DLL viene caricata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="23eb9-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="23eb9-107">Questa notifica si verifica prima che venga eseguito il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="23eb9-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="23eb9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23eb9-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="23eb9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="23eb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23eb9-110">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23eb9-111">Questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23eb9-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23eb9-112">*NotificationFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23eb9-113">Puntatore a una funzione di callback di notifica [*LdrDllNotification*](ldrdllnotification.md) da chiamare quando la dll viene caricata.</span><span class="sxs-lookup"><span data-stu-id="23eb9-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="23eb9-114">*Contesto* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23eb9-115">Puntatore ai dati di contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="23eb9-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="23eb9-116">*Cookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23eb9-117">Puntatore a una variabile per ricevere un identificatore per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="23eb9-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="23eb9-118">Questo identificatore viene utilizzato per annullare la registrazione della funzione di callback di notifica.</span><span class="sxs-lookup"><span data-stu-id="23eb9-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23eb9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23eb9-119">Return value</span></span>

<span data-ttu-id="23eb9-120">Se la funzione ha esito positivo, viene restituito **lo stato \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="23eb9-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="23eb9-121">I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.</span><span class="sxs-lookup"><span data-stu-id="23eb9-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="23eb9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="23eb9-122">Remarks</span></span>

<span data-ttu-id="23eb9-123">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="23eb9-123">This function has no associated header file.</span></span> <span data-ttu-id="23eb9-124">La libreria di importazione associata, Ntdll. lib, è disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="23eb9-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="23eb9-125">È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="23eb9-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="23eb9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23eb9-126">Requirements</span></span>



| <span data-ttu-id="23eb9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23eb9-127">Requirement</span></span> | <span data-ttu-id="23eb9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="23eb9-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23eb9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23eb9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23eb9-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="23eb9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23eb9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23eb9-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23eb9-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23eb9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="23eb9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23eb9-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23eb9-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23eb9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23eb9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23eb9-136">*LdrDllNotification*</span><span class="sxs-lookup"><span data-stu-id="23eb9-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="23eb9-137">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="23eb9-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
