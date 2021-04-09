---
description: Recupera una serie di informazioni per la batteria.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: Codice di controllo IOCTL_BATTERY_QUERY_INFORMATION (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967495"
---
# <a name="ioctl_battery_query_information-control-code"></a><span data-ttu-id="3758f-103">\_Codice di \_ \_ controllo delle informazioni sulle query della batteria IOCTL</span><span class="sxs-lookup"><span data-stu-id="3758f-103">IOCTL\_BATTERY\_QUERY\_INFORMATION control code</span></span>

<span data-ttu-id="3758f-104">Recupera una serie di informazioni per la batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-104">Retrieves a variety of information for the battery.</span></span>

<span data-ttu-id="3758f-105">Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="3758f-105">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="3758f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3758f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3758f-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3758f-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-108">Handle per la batteria in cui devono essere restituite le informazioni.</span><span class="sxs-lookup"><span data-stu-id="3758f-108">A handle to the battery on which information is to be returned.</span></span> <span data-ttu-id="3758f-109">Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="3758f-109">To retrieve a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-110">*dwIoControlCode*</span><span class="sxs-lookup"><span data-stu-id="3758f-110">*dwIoControlCode*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3758f-111">The control code for the operation.</span></span> <span data-ttu-id="3758f-112">Questo valore identifica l'operazione specifica da eseguire e il tipo di dispositivo su cui eseguirla.</span><span class="sxs-lookup"><span data-stu-id="3758f-112">This value identifies the specific operation to be performed and the type of device on which to perform it.</span></span> <span data-ttu-id="3758f-113">Usare **\_ \_ \_ le informazioni sulle query della batteria IOCTL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3758f-113">Use **IOCTL\_BATTERY\_QUERY\_INFORMATION** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="3758f-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-115">Puntatore a una struttura [**di \_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="3758f-115">A pointer to a [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-116">*nInBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3758f-116">*nInBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-117">Dimensioni in byte del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="3758f-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-118">*lpOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="3758f-118">*lpOutBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-119">Puntatore al buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="3758f-119">A pointer to the return buffer.</span></span> <span data-ttu-id="3758f-120">Il tipo di dati (e, di conseguenza, le dimensioni) del buffer restituito dipende dalle informazioni richieste nel membro **del \_ \_ \_ livello di informazioni** della query della batteria [**di \_ \_ input.**](battery-query-information-str.md)</span><span class="sxs-lookup"><span data-stu-id="3758f-120">The data type (and, therefore, size) of the return buffer depends on the information requested in the **BATTERY\_QUERY\_INFORMATION\_LEVEL** member of the input [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure.</span></span>

<span data-ttu-id="3758f-121">La tabella seguente mostra i dati restituiti da un determinato livello di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3758f-121">The following table shows the data returned by a given information level.</span></span>



| <span data-ttu-id="3758f-122">Livello informazioni</span><span class="sxs-lookup"><span data-stu-id="3758f-122">Information level</span></span>                 | <span data-ttu-id="3758f-123">Dati restituiti</span><span class="sxs-lookup"><span data-stu-id="3758f-123">Data returned</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3758f-124">**BatteryDeviceName**</span><span class="sxs-lookup"><span data-stu-id="3758f-124">**BatteryDeviceName**</span></span>             | <span data-ttu-id="3758f-125">Stringa Unicode con terminazione **null** che specifica il nome della batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-125">**Null**-terminated Unicode string that specifies the battery's name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3758f-126">**BatteryEstimatedTime**</span><span class="sxs-lookup"><span data-stu-id="3758f-126">**BatteryEstimatedTime**</span></span>          | <span data-ttu-id="3758f-127">**ULONG** che specifica il tempo di esecuzione della batteria stimato, in secondi.</span><span class="sxs-lookup"><span data-stu-id="3758f-127">A **ULONG** that specifies estimated battery run time, in seconds.</span></span> <span data-ttu-id="3758f-128">Se la frequenza di svuotamento fornita nel membro **AtRate** della struttura di [**\_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) è zero, questo calcolo è basato sulla velocità attuale di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="3758f-128">If the rate of drain provided in the **AtRate** member of the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure is zero, this calculation is based on the present rate of drain.</span></span> <span data-ttu-id="3758f-129">Se **AtRate** è diverso da zero, l'ora restituita è il tempo di esecuzione previsto per la velocità specificata.</span><span class="sxs-lookup"><span data-stu-id="3758f-129">If **AtRate** is nonzero, the time returned is the expected run time for the given rate.</span></span> <span data-ttu-id="3758f-130">Se il tempo stimato è sconosciuto (ad esempio, la batteria non viene ricaricata e **AtRate** è zero), viene restituita l' **\_ \_ ora della batteria sconosciuta** .</span><span class="sxs-lookup"><span data-stu-id="3758f-130">If the estimated time is unknown (for example, the battery is not discharging and **AtRate** is zero), **BATTERY\_UNKNOWN\_TIME** is returned.</span></span> <span data-ttu-id="3758f-131">Si noti che questo valore non è molto accurato in alcuni sistemi a batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-131">Note that this value is not very accurate on some battery systems.</span></span> <span data-ttu-id="3758f-132">Il valore può variare notevolmente a seconda del consumo di energia attuale, che può essere influenzato dall'attività del disco e da altri fattori.</span><span class="sxs-lookup"><span data-stu-id="3758f-132">The value may vary widely depending on present power usage, which could be affected by disk activity and other factors.</span></span> <span data-ttu-id="3758f-133">Non esiste alcun meccanismo di notifica delle modifiche in questo valore.</span><span class="sxs-lookup"><span data-stu-id="3758f-133">There is no notification mechanism for changes in this value.</span></span> |
| <span data-ttu-id="3758f-134">**BatteryGranularityInformation**</span><span class="sxs-lookup"><span data-stu-id="3758f-134">**BatteryGranularityInformation**</span></span> | <span data-ttu-id="3758f-135">Matrice a lunghezza variabile di strutture [**di \_ \_ scalabilità di report della batteria**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) che contiene la granularità dei report per la capacità della batteria restituita dallo [**\_ \_ \_ stato della query della batteria IOCTL**](ioctl-battery-query-status.md).</span><span class="sxs-lookup"><span data-stu-id="3758f-135">A variable-length array of [**BATTERY\_REPORTING\_SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) structures that contains the reporting granularity for the battery capacity that is returned from [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md).</span></span> <span data-ttu-id="3758f-136">Quando la granularità dipende dalla capacità attuale della batteria, vengono restituite più voci.</span><span class="sxs-lookup"><span data-stu-id="3758f-136">Multiple entries are returned when the granularity depends on the present capacity of the battery.</span></span> <span data-ttu-id="3758f-137">Vedere la pagina relativa alla **\_ \_ scalabilità dei report batteria** per l'interpretazione della matrice di voci.</span><span class="sxs-lookup"><span data-stu-id="3758f-137">See **BATTERY\_REPORTING\_SCALE** for the interpretation of the array of entries.</span></span> <span data-ttu-id="3758f-138">Il numero di voci è indicato dalla dimensione del buffer restituito e può essere calcolato come (*lpBytesReturned* /sizeof (**\_ \_ scala di report della batteria**)).</span><span class="sxs-lookup"><span data-stu-id="3758f-138">The number of entries is indicated by the size of the buffer returned, and can be calculated as (*lpBytesReturned* / sizeof (**BATTERY\_REPORTING\_SCALE**)).</span></span> <span data-ttu-id="3758f-139">Il numero massimo di voci che verranno restituite è quattro.</span><span class="sxs-lookup"><span data-stu-id="3758f-139">The maximum number of entries that will be returned is four.</span></span>                                                                                                |
| <span data-ttu-id="3758f-140">**BatteryInformation**</span><span class="sxs-lookup"><span data-stu-id="3758f-140">**BatteryInformation**</span></span>            | <span data-ttu-id="3758f-141">Struttura [**\_ delle informazioni sulla batteria**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="3758f-141">A [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3758f-142">**BatteryManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="3758f-142">**BatteryManufactureDate**</span></span>        | <span data-ttu-id="3758f-143">Struttura [**della \_ \_ Data di produzione della batteria**](battery-manufacture-date-str.md) .</span><span class="sxs-lookup"><span data-stu-id="3758f-143">A [**BATTERY\_MANUFACTURE\_DATE**](battery-manufacture-date-str.md) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="3758f-144">**BatteryManufactureName**</span><span class="sxs-lookup"><span data-stu-id="3758f-144">**BatteryManufactureName**</span></span>        | <span data-ttu-id="3758f-145">Stringa Unicode con terminazione **null** che contiene il nome del produttore della batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-145">**Null**-terminated Unicode string that contains the name of the manufacturer of the battery.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3758f-146">**BatterySerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3758f-146">**BatterySerialNumber**</span></span>           | <span data-ttu-id="3758f-147">Stringa Unicode con terminazione **null** che contiene il numero di serie della batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-147">**Null**-terminated Unicode string that contains the battery's serial number.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3758f-148">**BatteryTemperature**</span><span class="sxs-lookup"><span data-stu-id="3758f-148">**BatteryTemperature**</span></span>            | <span data-ttu-id="3758f-149">**ULONG** che contiene la temperatura corrente della batteria, in decimi di grado Kelvin.</span><span class="sxs-lookup"><span data-stu-id="3758f-149">A **ULONG** that contains the battery's current temperature, in 10ths of a degree Kelvin.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3758f-150">**BatteryUniqueID**</span><span class="sxs-lookup"><span data-stu-id="3758f-150">**BatteryUniqueID**</span></span>               | <span data-ttu-id="3758f-151">Stringa Unicode con terminazione **null** che identifica in modo univoco la batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-151">**Null**-terminated Unicode string that uniquely identifies the battery.</span></span> <span data-ttu-id="3758f-152">Questo valore può essere usato per tenere traccia di una batteria specifica.</span><span class="sxs-lookup"><span data-stu-id="3758f-152">This value can be used to track a specific battery.</span></span> <span data-ttu-id="3758f-153">Nel caso di batterie intelligenti, questo ID sarà la concatenazione del nome del produttore, del nome del dispositivo, della data di produzione e di una rappresentazione stampabile del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="3758f-153">In the case of smart batteries, this ID will be the concatenation of the manufacturer's name, device name, date of manufacture, and a printable representation of the serial number.</span></span> <span data-ttu-id="3758f-154">Questo valore non può essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="3758f-154">This value is not intended to be displayed to the user.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="3758f-155">*nOutBufferSize*</span><span class="sxs-lookup"><span data-stu-id="3758f-155">*nOutBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-156">Dimensioni in byte del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="3758f-156">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="3758f-157">A seconda del livello di informazioni dei dati richiesti, può trattarsi di un buffer di dimensioni variabili.</span><span class="sxs-lookup"><span data-stu-id="3758f-157">Depending on the information level of data requested, this may be a variably sized buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-158">*lpBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="3758f-158">*lpBytesReturned*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-159">Puntatore a una variabile che riceve la dimensione dei dati restituiti nel buffer *lpOutBuffer* , in byte.</span><span class="sxs-lookup"><span data-stu-id="3758f-159">A pointer to a variable that receives the size of the data returned in the *lpOutBuffer* buffer, in bytes.</span></span>

<span data-ttu-id="3758f-160">Se il buffer di output è troppo piccolo per restituire i dati, la chiamata ha esito negativo, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il **\_ \_ buffer insufficiente** nell'errore del codice di errore e il numero di byte restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3758f-160">If the output buffer is too small to return any data then the call fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code **ERROR\_INSUFFICIENT\_BUFFER**, and the returned byte count is zero.</span></span>

<span data-ttu-id="3758f-161">Se *lpOverlapped* è **null** (I/O non sovrapposti), *lpBytesReturned* non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3758f-161">If *lpOverlapped* is **NULL** (nonoverlapped I/O), *lpBytesReturned* cannot be **NULL**.</span></span>

<span data-ttu-id="3758f-162">Se *lpOverlapped* non è **null** (I/O sovrapposto), *lpBytesReturned* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3758f-162">If *lpOverlapped* is not **NULL** (overlapped I/O), *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="3758f-163">Se si tratta di un'operazione sovrapposta, è possibile recuperare il numero di byte restituiti chiamando la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="3758f-163">If this is an overlapped operation, you can retrieve the number of bytes returned by calling the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="3758f-164">Se *hDevice* è associato a una porta di completamento di I/O, è possibile ottenere il numero di byte restituiti chiamando la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3758f-164">If *hDevice* is associated with an I/O completion port, you can get the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="3758f-165">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="3758f-165">*lpOverlapped*</span></span> 
</dt> <dd>

<span data-ttu-id="3758f-166">Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="3758f-166">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="3758f-167">Se *hDevice* è stato aperto con il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="3758f-167">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="3758f-168">In questo caso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) viene eseguito come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="3758f-168">In this case, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="3758f-169">Se il dispositivo è stato aperto con il flag **file \_ \_ sovrapposto** e *lpOverlapped* è **null**, la funzione avrà esito negativo in modi imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="3758f-169">If the device was opened with the **FILE\_FLAG\_OVERLAPPED** flag and *lpOverlapped* is **NULL**, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="3758f-170">Se *hDevice* è stato aperto senza specificare il flag **\_ \_ OVERLAPPED del flag file** , *lpOverlapped* viene ignorato e la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) non viene restituita fino al completamento dell'operazione o fino a quando non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3758f-170">If *hDevice* was opened without specifying the **FILE\_FLAG\_OVERLAPPED** flag, *lpOverlapped* is ignored and the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function does not return until the operation has been completed, or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3758f-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3758f-171">Return value</span></span>

<span data-ttu-id="3758f-172">Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3758f-172">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="3758f-173">Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3758f-173">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="3758f-174">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3758f-174">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="3758f-175">Alcune informazioni sulle batterie sono facoltative o potrebbero non essere significative per alcune batterie.</span><span class="sxs-lookup"><span data-stu-id="3758f-175">Some information about batteries is optional or may be meaningless for some batteries.</span></span> <span data-ttu-id="3758f-176">Se il tipo specifico di dati richiesti non è disponibile per la batteria corrente, viene restituita la **\_ \_ funzione Error non valida** .</span><span class="sxs-lookup"><span data-stu-id="3758f-176">If the particular type of data requested is not available for the current battery, then **ERROR\_INVALID\_FUNCTION** is returned.</span></span>

<span data-ttu-id="3758f-177">Tutte le richieste di informazioni sulla batteria vengono completate con lo stato del **file di errore \_ \_ non \_ trovato** ogni volta che l'elemento **BatteryTag** della richiesta non corrisponde a quello del tag della batteria corrente.</span><span class="sxs-lookup"><span data-stu-id="3758f-177">All requests for battery information will complete with the status of **ERROR\_FILE\_NOT\_FOUND** whenever the **BatteryTag** element of the request does not match that of the current battery tag.</span></span> <span data-ttu-id="3758f-178">In questo modo si garantisce che le informazioni della batteria restituita corrispondano a quelle della batteria richiesta.</span><span class="sxs-lookup"><span data-stu-id="3758f-178">This ensures that the returned battery information matches that of the requested battery.</span></span> <span data-ttu-id="3758f-179">Per ulteriori informazioni, vedere la pagina relativa ai [tag della batteria](battery-information.md) .</span><span class="sxs-lookup"><span data-stu-id="3758f-179">(See [Battery Tags](battery-information.md) for more information.)</span></span>

## <a name="remarks"></a><span data-ttu-id="3758f-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="3758f-180">Remarks</span></span>

<span data-ttu-id="3758f-181">Questo comando IOCTL batteria recupera una serie di informazioni per la batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-181">This battery IOCTL retrieves a variety of information for the battery.</span></span> <span data-ttu-id="3758f-182">La struttura del parametro di input, [**\_ \_ informazioni sulle query della batteria**](battery-query-information-str.md), indica il tipo di informazioni da restituire e quando devono essere restituite le informazioni sulla batteria.</span><span class="sxs-lookup"><span data-stu-id="3758f-182">The input parameter structure, [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md), indicates the type of information to be returned and when the battery information should be returned.</span></span> <span data-ttu-id="3758f-183">Il tipo di dati e il contenuto del buffer di output variano in base ai dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="3758f-183">The data type and contents of the output buffer vary based on the data requested.</span></span>

<span data-ttu-id="3758f-184">Per le implicazioni dell'I/O sovrapposto in questa operazione, vedere la sezione Osservazioni dell'argomento [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="3758f-184">For the implications of overlapped I/O on this operation, see the Remarks section of the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="3758f-185">Esempio</span><span class="sxs-lookup"><span data-stu-id="3758f-185">Examples</span></span>

<span data-ttu-id="3758f-186">Per un esempio, vedere [enumerazione dei dispositivi a batteria](enumerating-battery-devices.md).</span><span class="sxs-lookup"><span data-stu-id="3758f-186">For an example, see [Enumerating Battery Devices](enumerating-battery-devices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3758f-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3758f-187">Requirements</span></span>



| <span data-ttu-id="3758f-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="3758f-188">Requirement</span></span> | <span data-ttu-id="3758f-189">Valore</span><span class="sxs-lookup"><span data-stu-id="3758f-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3758f-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3758f-190">Minimum supported client</span></span><br/> | <span data-ttu-id="3758f-191">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3758f-191">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="3758f-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3758f-192">Minimum supported server</span></span><br/> | <span data-ttu-id="3758f-193">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3758f-193">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="3758f-194">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3758f-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="3758f-195"><dt>Poclass. h; </dt> <dt>BatClass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="3758f-195"><dt>Poclass.h; </dt> <dt>BatClass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3758f-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3758f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3758f-197">Informazioni sulla batteria</span><span class="sxs-lookup"><span data-stu-id="3758f-197">Battery Information</span></span>](battery-information.md)
</dt> <dt>

[<span data-ttu-id="3758f-198">Codici di controllo del risparmio energia</span><span class="sxs-lookup"><span data-stu-id="3758f-198">Power Management Control Codes</span></span>](power-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="3758f-199">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="3758f-199">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="3758f-200">**\_informazioni sulle query della batteria \_**</span><span class="sxs-lookup"><span data-stu-id="3758f-200">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="3758f-201">**\_ \_ scalabilità report batteria**</span><span class="sxs-lookup"><span data-stu-id="3758f-201">**BATTERY\_REPORTING\_SCALE**</span></span>](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[<span data-ttu-id="3758f-202">**\_stato della \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3758f-202">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="3758f-203">**\_tag di \_ query della batteria IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3758f-203">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> <dt>

[<span data-ttu-id="3758f-204">**\_ \_ informazioni sui set di batterie IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="3758f-204">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

