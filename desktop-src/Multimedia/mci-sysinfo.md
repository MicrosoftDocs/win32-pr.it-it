---
title: Comando MCI_SYSINFO (mmsystem. h)
description: Il \_ comando MCI sysinfo recupera informazioni sui dispositivi MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Comando MCI_SYSINFO Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964329"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="b081e-104">\_Comando MCI sysinfo</span><span class="sxs-lookup"><span data-stu-id="b081e-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="b081e-105">Il \_ comando MCI sysinfo recupera informazioni sui dispositivi MCI.</span><span class="sxs-lookup"><span data-stu-id="b081e-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="b081e-106">MCI supporta direttamente questo comando anziché passarlo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b081e-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="b081e-107">Qualsiasi applicazione MCI può utilizzare questo comando.</span><span class="sxs-lookup"><span data-stu-id="b081e-107">Any MCI application can use this command.</span></span> <span data-ttu-id="b081e-108">Le informazioni sulla stringa vengono restituite nel buffer fornito dall'applicazione a cui fa riferimento il membro **lpstrReturn** della struttura identificata da *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="b081e-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="b081e-109">Le informazioni numeriche vengono restituite come valore **DWORD** inserito nel buffer fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b081e-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="b081e-110">Il membro **dwRetSize** specifica la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="b081e-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="b081e-111">Per inviare questo comando, chiamare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b081e-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b081e-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b081e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b081e-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b081e-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b081e-114">Identificatore del dispositivo MCI che deve ricevere il messaggio di comando.</span><span class="sxs-lookup"><span data-stu-id="b081e-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b081e-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b081e-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b081e-116">Uno o più dei seguenti flag standard e specifici del comando:</span><span class="sxs-lookup"><span data-stu-id="b081e-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="b081e-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>installazione di MCI \_ sysinfo \_</span><span class="sxs-lookup"><span data-stu-id="b081e-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="b081e-118">Ottiene il nome (elencato nel registro di sistema o il file di SYSTEM.INI) usato per installare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b081e-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="b081e-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nome della sysinfo MCI \_</span><span class="sxs-lookup"><span data-stu-id="b081e-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="b081e-120">Ottiene un nome di dispositivo corrispondente al numero di dispositivo specificato nel membro **dwNumber** della struttura identificata da **lpSysInfo**.</span><span class="sxs-lookup"><span data-stu-id="b081e-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="b081e-121">Se il \_ \_ flag di apertura di MCI sysinfo è impostato, MCI restituisce i nomi dei dispositivi aperti.</span><span class="sxs-lookup"><span data-stu-id="b081e-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="b081e-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>apertura di MCI \_ sysinfo \_</span><span class="sxs-lookup"><span data-stu-id="b081e-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="b081e-123">Ottiene la quantità o il nome dei dispositivi aperti.</span><span class="sxs-lookup"><span data-stu-id="b081e-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="b081e-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantità sysinfo \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b081e-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="b081e-125">Ottiene il numero di dispositivi del tipo specificato elencati nel registro di sistema o nella \[ \] sezione MCI del file di SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="b081e-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="b081e-126">Se \_ \_ è impostato il flag di apertura di MCI sysinfo, viene restituito il numero di dispositivi aperti.</span><span class="sxs-lookup"><span data-stu-id="b081e-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="b081e-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span><span class="sxs-lookup"><span data-stu-id="b081e-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="b081e-128">Puntatore a una [**struttura \_ \_ parametri di MCI sysinfo**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b081e-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b081e-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b081e-129">Return Value</span></span>

<span data-ttu-id="b081e-130">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="b081e-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b081e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b081e-131">Remarks</span></span>

<span data-ttu-id="b081e-132">Il membro **wDeviceType** della struttura identificata da *lpSysInfo* viene usato per indicare il tipo di dispositivo della query.</span><span class="sxs-lookup"><span data-stu-id="b081e-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="b081e-133">Se il parametro *wDeviceID* è impostato su MCI \_ All \_ Device \_ ID, viene eseguito l'override del valore di **wDeviceType**.</span><span class="sxs-lookup"><span data-stu-id="b081e-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="b081e-134">Per un elenco dei tipi di dispositivo, vedere [tipi di dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="b081e-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="b081e-135">I valori restituiti integer sono valori **DWORD** restituiti nel buffer a cui punta il membro **lpstrReturn** della struttura identificata da *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="b081e-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="b081e-136">I valori restituiti dalla stringa sono stringhe con terminazione null restituite nel buffer a cui punta il membro **lpstrReturn** della struttura identificata da *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="b081e-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b081e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b081e-137">Requirements</span></span>



| <span data-ttu-id="b081e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b081e-138">Requirement</span></span> | <span data-ttu-id="b081e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b081e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b081e-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b081e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b081e-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b081e-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b081e-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b081e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b081e-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b081e-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b081e-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b081e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b081e-145"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b081e-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b081e-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b081e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b081e-147">MCI</span><span class="sxs-lookup"><span data-stu-id="b081e-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b081e-148">Comandi MCI</span><span class="sxs-lookup"><span data-stu-id="b081e-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

