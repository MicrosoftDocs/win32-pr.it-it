---
title: Comando MCI_CONFIGURE (mmsystem. h)
description: Il \_ comando di configurazione di MCI Visualizza una finestra di dialogo per l'impostazione delle opzioni operative. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- Comando MCI_CONFIGURE Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400286"
---
# <a name="mci_configure-command"></a><span data-ttu-id="214d7-105">\_Comando di configurazione MCI</span><span class="sxs-lookup"><span data-stu-id="214d7-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="214d7-106">Il \_ comando di configurazione di MCI Visualizza una finestra di dialogo per l'impostazione delle opzioni operative.</span><span class="sxs-lookup"><span data-stu-id="214d7-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="214d7-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="214d7-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="214d7-108">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="214d7-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="214d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="214d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214d7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="214d7-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="214d7-111">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="214d7-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="214d7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="214d7-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="214d7-113">\_Test MCI notifica, MCI \_ Wait o MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="214d7-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="214d7-114">Per informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="214d7-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="214d7-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span><span class="sxs-lookup"><span data-stu-id="214d7-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="214d7-116">Puntatore a una [**struttura \_ \_ parametri generica MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="214d7-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="214d7-117">I dispositivi con set di comandi estesi possono sostituire questa struttura con una struttura specifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="214d7-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214d7-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="214d7-118">Return Value</span></span>

<span data-ttu-id="214d7-119">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="214d7-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="214d7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="214d7-120">Requirements</span></span>



| <span data-ttu-id="214d7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="214d7-121">Requirement</span></span> | <span data-ttu-id="214d7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="214d7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="214d7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="214d7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="214d7-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="214d7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="214d7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="214d7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="214d7-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="214d7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="214d7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="214d7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="214d7-128"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="214d7-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214d7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="214d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214d7-130">MCI</span><span class="sxs-lookup"><span data-stu-id="214d7-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="214d7-131">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="214d7-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

