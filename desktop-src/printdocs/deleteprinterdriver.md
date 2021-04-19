---
description: La funzione DeletePrinterDriver rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Funzione DeletePrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311549"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="613d5-103">DeletePrinterDriver (funzione)</span><span class="sxs-lookup"><span data-stu-id="613d5-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="613d5-104">La funzione **DeletePrinterDriver** rimuove il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati in un server.</span><span class="sxs-lookup"><span data-stu-id="613d5-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="613d5-105">Per eliminare i file associati al driver, oltre a rimuovere il nome del driver della stampante specificato dall'elenco dei nomi dei driver supportati per un server, utilizzare la funzione [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="613d5-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="613d5-106">**DeletePrinterDriver** Elimina un driver solo se non è in uso alcuna versione del driver per l'ambiente specificato.</span><span class="sxs-lookup"><span data-stu-id="613d5-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="613d5-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) può eliminare versioni specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="613d5-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="613d5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="613d5-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="613d5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="613d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613d5-110">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613d5-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613d5-111">Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere eliminato il driver.</span><span class="sxs-lookup"><span data-stu-id="613d5-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="613d5-112">Se questo parametro è **null**, il nome del driver della stampante verrà rimosso localmente.</span><span class="sxs-lookup"><span data-stu-id="613d5-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="613d5-113">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613d5-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613d5-114">Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere eliminato il driver (ad esempio, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="613d5-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="613d5-115">Se questo parametro è **null**, il nome del driver viene eliminato dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="613d5-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="613d5-116">*pDriverName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="613d5-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613d5-117">Puntatore a una stringa con terminazione null che specifica il nome del driver da eliminare.</span><span class="sxs-lookup"><span data-stu-id="613d5-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613d5-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="613d5-118">Return value</span></span>

<span data-ttu-id="613d5-119">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="613d5-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="613d5-120">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="613d5-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="613d5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="613d5-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="613d5-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="613d5-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="613d5-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="613d5-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="613d5-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="613d5-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="613d5-125">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="613d5-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="613d5-126">La funzione **DeletePrinterDriver** non elimina i file associati, ma rimuove semplicemente il nome del driver dall'elenco restituito dalla funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="613d5-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="613d5-127">Prima di chiamare **DeletePrinterDriver**, è necessario eliminare tutti gli oggetti stampante che usano il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="613d5-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="613d5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="613d5-128">Requirements</span></span>



| <span data-ttu-id="613d5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="613d5-129">Requirement</span></span> | <span data-ttu-id="613d5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="613d5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613d5-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613d5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="613d5-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613d5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="613d5-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="613d5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="613d5-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="613d5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="613d5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="613d5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="613d5-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="613d5-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="613d5-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="613d5-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="613d5-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="613d5-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="613d5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="613d5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613d5-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="613d5-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="613d5-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="613d5-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="613d5-142">**DeletePrinterDriverW** (Unicode) e **DeletePrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="613d5-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="613d5-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="613d5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613d5-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="613d5-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="613d5-145">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="613d5-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="613d5-146">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="613d5-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="613d5-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="613d5-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

