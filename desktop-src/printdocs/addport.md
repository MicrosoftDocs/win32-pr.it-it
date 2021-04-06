---
description: La funzione AddPort aggiunge il nome di una porta all'elenco delle porte supportate. La funzione AddPort viene esportata dal monitor di porta.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Funzione AddPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884989"
---
# <a name="addport-function"></a><span data-ttu-id="e85f6-104">AddPort (funzione)</span><span class="sxs-lookup"><span data-stu-id="e85f6-104">AddPort function</span></span>

<span data-ttu-id="e85f6-105">La funzione **addport** aggiunge il nome di una porta all'elenco delle porte supportate.</span><span class="sxs-lookup"><span data-stu-id="e85f6-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="e85f6-106">La funzione **addport** viene esportata dal monitor di porta.</span><span class="sxs-lookup"><span data-stu-id="e85f6-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85f6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e85f6-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="e85f6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e85f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e85f6-109">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e85f6-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e85f6-110">Puntatore a una stringa con terminazione zero che specifica il nome del server a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="e85f6-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="e85f6-111">Se questo parametro è **null**, la porta è locale.</span><span class="sxs-lookup"><span data-stu-id="e85f6-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="e85f6-112">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e85f6-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e85f6-113">Handle per la finestra padre della finestra di dialogo **addport** .</span><span class="sxs-lookup"><span data-stu-id="e85f6-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e85f6-114">*pMonitorName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e85f6-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e85f6-115">Puntatore a una stringa con terminazione zero che specifica il monitoraggio associato alla porta.</span><span class="sxs-lookup"><span data-stu-id="e85f6-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e85f6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e85f6-116">Return value</span></span>

<span data-ttu-id="e85f6-117">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e85f6-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e85f6-118">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="e85f6-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e85f6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e85f6-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e85f6-120">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e85f6-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e85f6-121">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e85f6-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e85f6-122">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="e85f6-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e85f6-123">La funzione **addport** Esplora la rete per individuare le porte esistenti e visualizza una finestra di dialogo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="e85f6-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="e85f6-124">La funzione **addport** deve convalidare il nome della porta immesso dall'utente chiamando [**EnumPorts**](enumports.md) per assicurarsi che non esistano nomi duplicati.</span><span class="sxs-lookup"><span data-stu-id="e85f6-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="e85f6-125">Il chiamante della funzione **addport** deve avere \_ accesso al server \_ per amministrare l'accesso al server a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="e85f6-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="e85f6-126">Per aggiungere una porta senza visualizzare una finestra di dialogo, chiamare la funzione **XcvData** anziché **addport**.</span><span class="sxs-lookup"><span data-stu-id="e85f6-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="e85f6-127">Per ulteriori informazioni su **XcvData**, vedere Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="e85f6-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="e85f6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e85f6-128">Requirements</span></span>



| <span data-ttu-id="e85f6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85f6-129">Requirement</span></span> | <span data-ttu-id="e85f6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e85f6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85f6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e85f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e85f6-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e85f6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e85f6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e85f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e85f6-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e85f6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e85f6-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e85f6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85f6-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e85f6-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e85f6-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="e85f6-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e85f6-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e85f6-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e85f6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e85f6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e85f6-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e85f6-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="e85f6-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e85f6-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e85f6-142">**AddPortW** (Unicode) e **AddPortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e85f6-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="e85f6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e85f6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85f6-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="e85f6-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e85f6-145">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="e85f6-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e85f6-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="e85f6-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="e85f6-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="e85f6-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="e85f6-148">**Porta**</span><span class="sxs-lookup"><span data-stu-id="e85f6-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




