---
description: La funzione DocumentProperties recupera o modifica le informazioni di inizializzazione della stampante o Visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Funzione DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131910"
---
# <a name="documentproperties-function"></a><span data-ttu-id="7c148-103">DocumentProperties (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c148-103">DocumentProperties function</span></span>

<span data-ttu-id="7c148-104">La funzione **DocumentProperties** Recupera o modifica le informazioni di inizializzazione della stampante o Visualizza una finestra delle proprietà di configurazione della stampante per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="7c148-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c148-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c148-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="7c148-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c148-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c148-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-108">Handle per la finestra padre della finestra delle proprietà di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="7c148-109">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c148-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-110">Handle per un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="7c148-110">A handle to a printer object.</span></span> <span data-ttu-id="7c148-111">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="7c148-112">*pDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c148-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-113">Puntatore a una stringa con terminazione null che specifica il nome del dispositivo per il quale viene visualizzata la finestra delle proprietà di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="7c148-114">*pDevModeOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c148-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-115">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che riceve i dati di configurazione della stampante specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c148-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="7c148-116">*pDevModeInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c148-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-117">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) utilizzata dal sistema operativo per inizializzare i controlli della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7c148-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="7c148-118">Questo parametro viene utilizzato solo se il flag **DM \_ in \_ buffer** è impostato nel parametro *fmode* .</span><span class="sxs-lookup"><span data-stu-id="7c148-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="7c148-119">Se **DM \_ in \_ buffer** non è impostato, il sistema operativo usa la funzione [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)predefinita della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="7c148-120">*fmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c148-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c148-121">Operazioni eseguite dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="7c148-121">The operations the function performs.</span></span> <span data-ttu-id="7c148-122">Se questo parametro è zero, la funzione **DocumentProperties** restituisce il numero di byte necessari per la struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="7c148-123">In caso contrario, utilizzare una o più delle seguenti costanti per costruire un valore per questo parametro. Si noti, tuttavia, che per modificare le impostazioni di stampa, un'applicazione deve specificare almeno un valore di input e un valore di output.</span><span class="sxs-lookup"><span data-stu-id="7c148-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="7c148-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7c148-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="7c148-125">Significato</span><span class="sxs-lookup"><span data-stu-id="7c148-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="7c148-126"><dt>**DM \_ in \_ buffer**</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="7c148-127">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="7c148-127">Input value.</span></span> <span data-ttu-id="7c148-128">Prima di richiedere, copiare o aggiornare, la funzione unisce le impostazioni di stampa correnti del driver della stampante con le impostazioni nella struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal parametro *pDevModeInput* .</span><span class="sxs-lookup"><span data-stu-id="7c148-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="7c148-129">La funzione aggiorna la struttura solo per i membri specificati dal membro **dmFields** della struttura **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="7c148-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="7c148-130">Questo valore è definito anche come **DM \_ Modify**.</span><span class="sxs-lookup"><span data-stu-id="7c148-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="7c148-131">In caso di conflitto durante l'Unione, le impostazioni nella struttura **DEVMODE** specificata da *pDevModeInput* sostituiscono le impostazioni di stampa correnti del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="7c148-132"><dt>**DM \_ nella \_ richiesta**</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="7c148-133">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="7c148-133">Input value.</span></span> <span data-ttu-id="7c148-134">La funzione Visualizza la finestra delle proprietà di installazione di stampa del driver della stampante e quindi modifica le impostazioni nella struttura dei dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) della stampante in base ai valori specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c148-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="7c148-135">Questo valore viene definito anche come **\_ prompt DM**.</span><span class="sxs-lookup"><span data-stu-id="7c148-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="7c148-136"><dt>**\_buffer out \_ DM**</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="7c148-137">Valore di output.</span><span class="sxs-lookup"><span data-stu-id="7c148-137">Output value.</span></span> <span data-ttu-id="7c148-138">La funzione scrive le impostazioni di stampa correnti del driver della stampante, inclusi i dati privati, nella struttura di dati [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) specificata dal parametro *pDevModeOutput* .</span><span class="sxs-lookup"><span data-stu-id="7c148-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="7c148-139">Il chiamante deve allocare un buffer sufficientemente grande per contenere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7c148-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="7c148-140">Se il set **di \_ \_ buffer di bit DM out** è chiaro, il parametro *pDevModeOutput* può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7c148-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="7c148-141">Questo valore è definito anche **\_ copia DM**.</span><span class="sxs-lookup"><span data-stu-id="7c148-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c148-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c148-142">Return value</span></span>

<span data-ttu-id="7c148-143">Se il parametro *fmode* è zero, il valore restituito corrisponde alla dimensione del buffer necessaria per contenere i dati di inizializzazione del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="7c148-144">Si noti che questo buffer può essere più grande di una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) se il driver della stampante aggiunge dati privati alla struttura.</span><span class="sxs-lookup"><span data-stu-id="7c148-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="7c148-145">Se la funzione Visualizza la finestra delle proprietà, il valore restituito è **IDOK** o **IDCANCEL**, a seconda del pulsante selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c148-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="7c148-146">Se la funzione non Visualizza la finestra delle proprietà e ha esito positivo, il valore restituito è **IDOK**.</span><span class="sxs-lookup"><span data-stu-id="7c148-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="7c148-147">Se la funzione ha esito negativo, il valore restituito è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="7c148-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c148-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c148-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7c148-149">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7c148-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7c148-150">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c148-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7c148-151">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="7c148-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="7c148-152">La stringa a cui punta il parametro *pDeviceName* può essere ottenuta chiamando la funzione [**GetPrinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="7c148-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="7c148-153">La struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) effettivamente utilizzata da un driver della stampante contiene la parte indipendente dal dispositivo (come definito in precedenza) seguita da una parte specifica del driver che varia in base alla dimensione e al contenuto con ogni driver e versione del driver.</span><span class="sxs-lookup"><span data-stu-id="7c148-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="7c148-154">A causa di questa dipendenza del driver, è molto importante per le applicazioni eseguire una query sul driver per la corretta dimensione della struttura **DEVMODE** prima di allocare un buffer.</span><span class="sxs-lookup"><span data-stu-id="7c148-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="7c148-155">**Per apportare modifiche alle impostazioni di stampa locali per un'applicazione, è necessario eseguire le operazioni seguenti:**</span><span class="sxs-lookup"><span data-stu-id="7c148-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="7c148-156">Ottenere il numero di byte necessari per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa chiamando **DocumentProperties** e specificando zero nel parametro *fmode* .</span><span class="sxs-lookup"><span data-stu-id="7c148-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="7c148-157">Allocare memoria per la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.</span><span class="sxs-lookup"><span data-stu-id="7c148-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="7c148-158">Ottenere le impostazioni della stampante correnti chiamando **DocumentProperties**.</span><span class="sxs-lookup"><span data-stu-id="7c148-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="7c148-159">Passare un puntatore alla struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) allocata nel passaggio 2 come parametro *pDevModeOutput* e specificare il valore **del \_ \_ buffer out di DM** .</span><span class="sxs-lookup"><span data-stu-id="7c148-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="7c148-160">Modificare i membri appropriati della struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) restituita e indicare i membri modificati impostando i bit corrispondenti nel membro **DmFields** dell'oggetto **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="7c148-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="7c148-161">Chiamare **DocumentProperties** e passare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificata come entrambi i parametri *pDevModeInput* e *pDevModeOutput* e specificare sia il **DM \_ in \_ buffer** che i valori del **\_ \_ buffer out DM** (combinati con l'operatore OR). La struttura **DEVMODE** restituita dalla terza chiamata a **DocumentProperties** può essere utilizzata come argomento in una chiamata alla funzione [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .</span><span class="sxs-lookup"><span data-stu-id="7c148-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="7c148-162">Per creare un handle per un contesto di dispositivo stampante usando le impostazioni della stampante correnti, è sufficiente chiamare **DocumentProperties** due volte, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7c148-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="7c148-163">La prima chiamata ottiene le dimensioni dell'oggetto [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo e la seconda chiamata Inizializza il **DEVMODE** con le impostazioni della stampante correnti.</span><span class="sxs-lookup"><span data-stu-id="7c148-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="7c148-164">Passare l'oggetto **DEVMODE** inizializzato a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) per ottenere l'handle per il contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="7c148-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c148-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c148-165">Requirements</span></span>



| <span data-ttu-id="7c148-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c148-166">Requirement</span></span> | <span data-ttu-id="7c148-167">Valore</span><span class="sxs-lookup"><span data-stu-id="7c148-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c148-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c148-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7c148-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c148-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c148-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c148-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7c148-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c148-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c148-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c148-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c148-173"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7c148-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c148-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c148-175"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7c148-176">DLL</span><span class="sxs-lookup"><span data-stu-id="7c148-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c148-177"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="7c148-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7c148-178">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7c148-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c148-179">**DocumentPropertiesW** (Unicode) e **DocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7c148-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7c148-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c148-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c148-181">Stampa</span><span class="sxs-lookup"><span data-stu-id="7c148-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7c148-182">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7c148-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7c148-183">**AdvancedDocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="7c148-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="7c148-184">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="7c148-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="7c148-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="7c148-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="7c148-186">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="7c148-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="7c148-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="7c148-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

