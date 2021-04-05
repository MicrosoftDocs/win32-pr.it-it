---
description: La funzione AddPrinterDriver installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Funzione AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757859"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="1bb5e-103">AddPrinterDriver (funzione)</span><span class="sxs-lookup"><span data-stu-id="1bb5e-103">AddPrinterDriver function</span></span>

<span data-ttu-id="1bb5e-104">La funzione **AddPrinterDriver** installa un driver della stampante locale o remoto e associa i file di configurazione, i dati e i driver.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="1bb5e-105">Per una maggiore flessibilità nell'installazione o nell'aggiornamento dei driver della stampante, utilizzare la funzione [**AddPrinterDriverEx**](addprinterdriverex.md) perché consente l'aggiornamento rigoroso, il downgrade rigoroso, la copia dei soli file più recenti e la copia di tutti i file (indipendentemente dagli indicatori di data e ora).</span><span class="sxs-lookup"><span data-stu-id="1bb5e-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="1bb5e-106">Non è più consigliabile installare un driver della stampante senza un pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="1bb5e-107">In alternativa, usare [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb5e-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1bb5e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bb5e-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1bb5e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bb5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb5e-110">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bb5e-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb5e-111">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il driver.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="1bb5e-112">Se *pname* è **null**, il driver verrà installato localmente.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="1bb5e-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1bb5e-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb5e-114">Versione della struttura a cui punta *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="1bb5e-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="1bb5e-115">Questo valore può essere 2, 3, 4, 6 o 8.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="1bb5e-116">*pDriverInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bb5e-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb5e-117">Puntatore a una struttura contenente informazioni sul driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="1bb5e-118">Dipende dal valore di *Level*.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="1bb5e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb5e-119">Value</span></span> | <span data-ttu-id="1bb5e-120">Struttura unità stampante</span><span class="sxs-lookup"><span data-stu-id="1bb5e-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="1bb5e-121">2</span><span class="sxs-lookup"><span data-stu-id="1bb5e-121">2</span></span>     | [<span data-ttu-id="1bb5e-122">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="1bb5e-123">3</span><span class="sxs-lookup"><span data-stu-id="1bb5e-123">3</span></span>     | [<span data-ttu-id="1bb5e-124">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="1bb5e-125">4</span><span class="sxs-lookup"><span data-stu-id="1bb5e-125">4</span></span>     | [<span data-ttu-id="1bb5e-126">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="1bb5e-127">6</span><span class="sxs-lookup"><span data-stu-id="1bb5e-127">6</span></span>     | [<span data-ttu-id="1bb5e-128">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="1bb5e-129">8</span><span class="sxs-lookup"><span data-stu-id="1bb5e-129">8</span></span>     | [<span data-ttu-id="1bb5e-130">**\_Informazioni driver \_ 8**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="1bb5e-131">Se il membro **pEnvironment** della struttura a cui punta *pDriverInfo* è **null**, viene usato l'ambiente corrente del chiamante/client (non di destinazione/Server).</span><span class="sxs-lookup"><span data-stu-id="1bb5e-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb5e-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bb5e-132">Return value</span></span>

<span data-ttu-id="1bb5e-133">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1bb5e-134">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb5e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bb5e-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1bb5e-136">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1bb5e-137">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1bb5e-138">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1bb5e-139">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="1bb5e-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="1bb5e-140">Prima che un'applicazione chiami la funzione **AddPrinterDriver** , tutti i file richiesti dal driver devono essere copiati nella directory di driver della stampante del sistema.</span><span class="sxs-lookup"><span data-stu-id="1bb5e-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="1bb5e-141">Un'applicazione può recuperare il nome di questa directory chiamando la funzione [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb5e-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="1bb5e-142">Un'applicazione può determinare quali driver della stampante sono attualmente installati chiamando la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="1bb5e-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb5e-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bb5e-143">Requirements</span></span>



| <span data-ttu-id="1bb5e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb5e-144">Requirement</span></span> | <span data-ttu-id="1bb5e-145">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb5e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb5e-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb5e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb5e-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1bb5e-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1bb5e-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb5e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb5e-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1bb5e-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1bb5e-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bb5e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bb5e-151"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bb5e-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1bb5e-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="1bb5e-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bb5e-153"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bb5e-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1bb5e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1bb5e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bb5e-155"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1bb5e-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1bb5e-156">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1bb5e-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1bb5e-157">**AddPrinterDriverW** (Unicode) e **AddPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1bb5e-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="1bb5e-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bb5e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb5e-159">Stampa</span><span class="sxs-lookup"><span data-stu-id="1bb5e-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-160">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="1bb5e-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-161">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-162">**\_Informazioni driver \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-163">**\_Informazioni driver \_ 3**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-164">**\_Informazioni driver \_ 4**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-165">**\_Informazioni driver \_ 6**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-166">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1bb5e-167">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="1bb5e-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

