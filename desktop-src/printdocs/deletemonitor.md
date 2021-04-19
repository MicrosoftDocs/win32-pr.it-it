---
description: La funzione DeleteMonitor rimuove un monitor di porta aggiunto dalla funzione AddMonitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Funzione DeleteMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311554"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="b6056-103">DeleteMonitor (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6056-103">DeleteMonitor function</span></span>

<span data-ttu-id="b6056-104">La funzione **DeleteMonitor** rimuove un monitor di porta aggiunto dalla funzione [**AddMonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="b6056-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6056-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6056-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="b6056-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6056-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6056-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6056-108">Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere rimosso il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b6056-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="b6056-109">Se questo parametro è **null**, il monitoraggio della porta viene rimosso localmente.</span><span class="sxs-lookup"><span data-stu-id="b6056-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="b6056-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6056-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6056-111">Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere rimosso il monitoraggio (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="b6056-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="b6056-112">Se questo parametro è **null**, il monitoraggio viene rimosso dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="b6056-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="b6056-113">*pMonitorName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6056-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6056-114">Puntatore a una stringa con terminazione null che specifica il nome del monitoraggio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b6056-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6056-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6056-115">Return value</span></span>

<span data-ttu-id="b6056-116">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b6056-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b6056-117">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b6056-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6056-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6056-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6056-119">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b6056-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b6056-120">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b6056-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b6056-121">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="b6056-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b6056-122">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="b6056-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6056-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6056-123">Requirements</span></span>



| <span data-ttu-id="b6056-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6056-124">Requirement</span></span> | <span data-ttu-id="b6056-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b6056-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6056-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6056-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b6056-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6056-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b6056-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6056-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b6056-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6056-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6056-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6056-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6056-131"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6056-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b6056-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6056-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6056-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6056-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b6056-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b6056-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6056-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b6056-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b6056-136">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b6056-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6056-137">**DeleteMonitorW** (Unicode) e **DeleteMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6056-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="b6056-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6056-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6056-139">Stampa</span><span class="sxs-lookup"><span data-stu-id="b6056-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6056-140">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="b6056-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b6056-141">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="b6056-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

