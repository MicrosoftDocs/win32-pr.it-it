---
description: La funzione seport imposta lo stato associato a una porta stampante.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Funzione seport (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049968"
---
# <a name="setport-function"></a><span data-ttu-id="36dfb-103">Funzione seport</span><span class="sxs-lookup"><span data-stu-id="36dfb-103">SetPort function</span></span>

<span data-ttu-id="36dfb-104">La funzione **seport** imposta lo stato associato a una porta stampante.</span><span class="sxs-lookup"><span data-stu-id="36dfb-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="36dfb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36dfb-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="36dfb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="36dfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36dfb-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36dfb-108">Puntatore a una stringa con terminazione zero che specifica il nome del server di stampa a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="36dfb-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="36dfb-109">Impostare questo parametro su **null** se la porta si trova nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="36dfb-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="36dfb-110">*pPortName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36dfb-111">Puntatore a una stringa con terminazione zero che specifica il nome della porta stampante.</span><span class="sxs-lookup"><span data-stu-id="36dfb-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="36dfb-112">*dwLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36dfb-113">Specifica il tipo di struttura a cui punta il parametro *pPortInfo* .</span><span class="sxs-lookup"><span data-stu-id="36dfb-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="36dfb-114">Questo valore deve essere 3, che corrisponde a una struttura di dati [**Port \_ info \_ 3**](port-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="36dfb-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="36dfb-115">*pPortInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36dfb-116">Puntatore a una struttura di [**informazioni sulla porta \_ \_ 3**](port-info-3.md) che contiene le informazioni sullo stato della porta da impostare.</span><span class="sxs-lookup"><span data-stu-id="36dfb-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36dfb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36dfb-117">Return value</span></span>

<span data-ttu-id="36dfb-118">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="36dfb-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="36dfb-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="36dfb-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="36dfb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="36dfb-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="36dfb-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="36dfb-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="36dfb-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36dfb-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="36dfb-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="36dfb-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="36dfb-124">Il chiamante della funzione **seport** deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="36dfb-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="36dfb-125">Inoltre, se il chiamante è un monitor della porta o del linguaggio, deve chiamare [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) per interrompere la rappresentazione prima di chiamare la **porta**.</span><span class="sxs-lookup"><span data-stu-id="36dfb-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="36dfb-126">Tutti i programmi che chiamano la **porta** \_ di accesso al server devono disporre dell'accesso al server \_ per amministrare l'accesso al server a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="36dfb-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="36dfb-127">Quando si imposta un valore di stato porta stampante con l' \_ errore tipo di stato porta valore gravità \_ \_ , lo spooler di stampa interrompe l'invio di processi alla porta.</span><span class="sxs-lookup"><span data-stu-id="36dfb-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="36dfb-128">Lo spooler di stampa riprende l'invio di processi alla porta quando lo stato della porta viene cancellato da un'altra chiamata a **seport**.</span><span class="sxs-lookup"><span data-stu-id="36dfb-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36dfb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36dfb-129">Requirements</span></span>



| <span data-ttu-id="36dfb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="36dfb-130">Requirement</span></span> | <span data-ttu-id="36dfb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="36dfb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dfb-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36dfb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="36dfb-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36dfb-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36dfb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="36dfb-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36dfb-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36dfb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36dfb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dfb-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36dfb-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="36dfb-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="36dfb-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="36dfb-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36dfb-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="36dfb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="36dfb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36dfb-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="36dfb-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="36dfb-142">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="36dfb-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="36dfb-143">**SetPortW** (Unicode) e **seporta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="36dfb-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="36dfb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36dfb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36dfb-145">Stampa</span><span class="sxs-lookup"><span data-stu-id="36dfb-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="36dfb-146">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="36dfb-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="36dfb-147">**Informazioni sulla porta \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="36dfb-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

