---
description: Funzione di callback di notifica specificata con la funzione LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Funzione di callback LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877218"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="21208-103">Funzione di callback LdrDllNotification</span><span class="sxs-lookup"><span data-stu-id="21208-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="21208-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="21208-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="21208-105">Funzione di callback di notifica specificata con la funzione [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="21208-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="21208-106">Il caricatore chiama questa funzione quando una DLL viene caricata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="21208-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="21208-107">**Avviso:** Non è sicuro che la funzione di callback delle notifiche chiami le funzioni in qualsiasi DLL.</span><span class="sxs-lookup"><span data-stu-id="21208-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="21208-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21208-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="21208-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21208-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21208-110">*NotificationReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21208-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21208-111">Motivo per cui è stata chiamata la funzione di callback di notifica.</span><span class="sxs-lookup"><span data-stu-id="21208-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="21208-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="21208-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="21208-113">Valore</span><span class="sxs-lookup"><span data-stu-id="21208-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="21208-114">Significato</span><span class="sxs-lookup"><span data-stu-id="21208-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="21208-115"><dt>**LDR \_ \_Motivo della notifica dll \_ \_ caricato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="21208-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="21208-116">La DLL è stata caricata.</span><span class="sxs-lookup"><span data-stu-id="21208-116">The DLL was loaded.</span></span> <span data-ttu-id="21208-117">Il parametro *NotificationData* punta a una struttura di **\_ \_ \_ \_ dati di notifica caricata dalla dll LDR** .</span><span class="sxs-lookup"><span data-stu-id="21208-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="21208-118"><dt>**LDR \_ \_Motivo della notifica dll \_ \_ scaricato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="21208-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="21208-119">La DLL è stata scaricata.</span><span class="sxs-lookup"><span data-stu-id="21208-119">The DLL was unloaded.</span></span> <span data-ttu-id="21208-120">Il parametro *NotificationData* punta a una struttura di dati di **\_ \_ \_ notifica non \_ caricata della dll LDR** .</span><span class="sxs-lookup"><span data-stu-id="21208-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="21208-121">*NotificationData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21208-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21208-122">Puntatore a un'Unione di **\_ \_ notifiche della dll LDR** costante che contiene i dati di notifica.</span><span class="sxs-lookup"><span data-stu-id="21208-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="21208-123">Questa Unione presenta la definizione seguente:</span><span class="sxs-lookup"><span data-stu-id="21208-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="21208-124">La **struttura \_ \_ \_ \_ dei dati di notifica caricati della dll LDR** presenta la seguente definizione:</span><span class="sxs-lookup"><span data-stu-id="21208-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="21208-125">La **struttura \_ \_ \_ \_ dei dati di notifica di LDR dll non caricata** presenta la seguente definizione:</span><span class="sxs-lookup"><span data-stu-id="21208-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="21208-126">*Contesto* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="21208-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="21208-127">Puntatore ai dati di contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="21208-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21208-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21208-128">Return value</span></span>

<span data-ttu-id="21208-129">Questa funzione di callback non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="21208-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21208-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="21208-130">Remarks</span></span>

<span data-ttu-id="21208-131">La funzione di callback delle notifiche viene chiamata prima che venga eseguita la connessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="21208-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="21208-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21208-132">Requirements</span></span>



| <span data-ttu-id="21208-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="21208-133">Requirement</span></span> | <span data-ttu-id="21208-134">Valore</span><span class="sxs-lookup"><span data-stu-id="21208-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="21208-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21208-135">Minimum supported client</span></span><br/> | <span data-ttu-id="21208-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21208-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="21208-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21208-137">Minimum supported server</span></span><br/> | <span data-ttu-id="21208-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21208-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21208-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21208-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21208-140">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="21208-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="21208-141">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="21208-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




