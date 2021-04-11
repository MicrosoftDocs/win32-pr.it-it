---
title: Comando MCI_CLOSE (mmsystem. h)
description: Il \_ comando MCI Close rilascia l'accesso a un dispositivo o a un file. Tutti i dispositivi riconoscono questo comando.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- Comando MCI_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119550"
---
# <a name="mci_close-command"></a><span data-ttu-id="c8a44-105">\_Comando di chiusura MCI</span><span class="sxs-lookup"><span data-stu-id="c8a44-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="c8a44-106">Il \_ comando MCI Close rilascia l'accesso a un dispositivo o a un file.</span><span class="sxs-lookup"><span data-stu-id="c8a44-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="c8a44-107">Tutti i dispositivi riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="c8a44-107">All devices recognize this command.</span></span>

<span data-ttu-id="c8a44-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8a44-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="c8a44-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8a44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a44-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c8a44-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c8a44-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="c8a44-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c8a44-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c8a44-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c8a44-113">\_Attesa notifica MCI o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c8a44-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="c8a44-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c8a44-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8a44-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span><span class="sxs-lookup"><span data-stu-id="c8a44-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="c8a44-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a44-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c8a44-117">È anche possibile usare una struttura **\_ \_ parametri di chiusura MCI** .</span><span class="sxs-lookup"><span data-stu-id="c8a44-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="c8a44-118">Per ulteriori informazioni, vedere i commenti per **\_ \_ parametri generici MCI**.</span><span class="sxs-lookup"><span data-stu-id="c8a44-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a44-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8a44-119">Return Value</span></span>

<span data-ttu-id="c8a44-120">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c8a44-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a44-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8a44-121">Remarks</span></span>

<span data-ttu-id="c8a44-122">Uscire da un'applicazione senza chiudere i dispositivi MCI aperti può lasciare inaccessibile il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8a44-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="c8a44-123">L'applicazione deve chiudere in modo esplicito ogni dispositivo o file al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c8a44-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="c8a44-124">MCI Scarica il dispositivo quando vengono chiuse tutte le istanze del dispositivo o tutti i file associati.</span><span class="sxs-lookup"><span data-stu-id="c8a44-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a44-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8a44-125">Requirements</span></span>



| <span data-ttu-id="c8a44-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a44-126">Requirement</span></span> | <span data-ttu-id="c8a44-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c8a44-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a44-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8a44-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a44-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8a44-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8a44-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8a44-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a44-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8a44-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8a44-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8a44-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8a44-133"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8a44-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a44-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8a44-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a44-135">MCI</span><span class="sxs-lookup"><span data-stu-id="c8a44-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c8a44-136">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="c8a44-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

