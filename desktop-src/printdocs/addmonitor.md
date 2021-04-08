---
description: La funzione AddMonitor installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Funzione AddMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058246"
---
# <a name="addmonitor-function"></a><span data-ttu-id="b0326-103">AddMonitor (funzione)</span><span class="sxs-lookup"><span data-stu-id="b0326-103">AddMonitor function</span></span>

<span data-ttu-id="b0326-104">La funzione **AddMonitor** installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b0326-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0326-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0326-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="b0326-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0326-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0326-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0326-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b0326-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="b0326-109">Per i sistemi che supportano solo l'installazione locale dei monitoraggi, la stringa deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b0326-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0326-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b0326-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0326-111">Versione della struttura a cui punta *pMonitors* .</span><span class="sxs-lookup"><span data-stu-id="b0326-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="b0326-112">Questo valore deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="b0326-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="b0326-113">*pMonitors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0326-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0326-114">Puntatore a una struttura di [**monitoraggio \_ info \_ 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b0326-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="b0326-115">Se il membro **pEnvironment** della struttura *pMonitors* è **null**, viene utilizzato l'ambiente corrente del chiamante (client), non della destinazione (Server).</span><span class="sxs-lookup"><span data-stu-id="b0326-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="b0326-116">Si noti che la chiamata avrà esito negativo se l'ambiente non corrisponde all'ambiente del server, ovvero è possibile aggiungere solo un monitoraggio scritto per l'architettura del server.</span><span class="sxs-lookup"><span data-stu-id="b0326-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0326-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0326-117">Return value</span></span>

<span data-ttu-id="b0326-118">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b0326-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b0326-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b0326-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0326-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0326-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0326-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b0326-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b0326-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0326-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b0326-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="b0326-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b0326-124">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="b0326-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="b0326-125">Prima che un'applicazione chiami la funzione **AddMonitor** , tutti i file richiesti dal monitoraggio devono essere copiati nella directory system32.</span><span class="sxs-lookup"><span data-stu-id="b0326-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="b0326-126">Per determinare i monitoraggi delle porte attualmente installati, chiamare la funzione [**EnumMonitors**](enummonitors.md) .</span><span class="sxs-lookup"><span data-stu-id="b0326-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="b0326-127">Per rimuovere un monitoraggio aggiunto da **AddMonitor**, chiamare la funzione [**DeleteMonitor**](deletemonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="b0326-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0326-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0326-128">Requirements</span></span>



| <span data-ttu-id="b0326-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0326-129">Requirement</span></span> | <span data-ttu-id="b0326-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b0326-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0326-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0326-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0326-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0326-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0326-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0326-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0326-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0326-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0326-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0326-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0326-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0326-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b0326-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0326-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0326-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0326-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b0326-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b0326-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0326-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b0326-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b0326-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b0326-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0326-142">**AddMonitorW** (Unicode) e **AddMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0326-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="b0326-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0326-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0326-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="b0326-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b0326-145">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="b0326-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b0326-146">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="b0326-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="b0326-147">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="b0326-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="b0326-148">**Informazioni sul monitoraggio \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b0326-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

