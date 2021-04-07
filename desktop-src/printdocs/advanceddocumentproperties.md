---
description: La funzione AdvancedDocumentProperties Visualizza una finestra di dialogo di configurazione della stampante per la stampante specificata, consentendo all'utente di configurare la stampante.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Funzione AdvancedDocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759560"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="9f20e-103">AdvancedDocumentProperties (funzione)</span><span class="sxs-lookup"><span data-stu-id="9f20e-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="9f20e-104">La funzione **AdvancedDocumentProperties** Visualizza una finestra di dialogo di configurazione della stampante per la stampante specificata, consentendo all'utente di configurare la stampante.</span><span class="sxs-lookup"><span data-stu-id="9f20e-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="9f20e-105">Questa funzione è un caso speciale della funzione [**DocumentProperties**](documentproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="9f20e-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="9f20e-106">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9f20e-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f20e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f20e-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="9f20e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f20e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f20e-109">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f20e-110">Handle per la finestra padre della finestra di dialogo Printer-Configuration.</span><span class="sxs-lookup"><span data-stu-id="9f20e-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9f20e-111">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f20e-112">Handle per un oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="9f20e-112">A handle to a printer object.</span></span> <span data-ttu-id="9f20e-113">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="9f20e-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9f20e-114">*pDeviceName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f20e-115">Puntatore a una stringa con terminazione null che specifica il nome del dispositivo per il quale deve essere visualizzata una finestra di dialogo di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="9f20e-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9f20e-116">*pDevModeOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f20e-117">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che conterrà i dati di configurazione specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9f20e-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="9f20e-118">*pDevModeInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f20e-119">Puntatore a una struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) che contiene i dati di configurazione utilizzati per inizializzare i controlli della finestra di dialogo di configurazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="9f20e-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f20e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f20e-120">Return value</span></span>

<span data-ttu-id="9f20e-121">Se la funzione [**DocumentProperties**](documentproperties.md) con questi parametri ha esito positivo, il valore restituito di **AdvancedDocumentProperties** è 1.</span><span class="sxs-lookup"><span data-stu-id="9f20e-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="9f20e-122">In caso contrario, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="9f20e-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f20e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f20e-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f20e-124">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="9f20e-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9f20e-125">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f20e-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9f20e-126">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="9f20e-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9f20e-127">Questa funzione può visualizzare solo la finestra di dialogo di configurazione della stampante, in modo che un utente possa configurarla.</span><span class="sxs-lookup"><span data-stu-id="9f20e-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="9f20e-128">Per un maggiore controllo, usare [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="9f20e-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="9f20e-129">I parametri di input per questa funzione vengono passati direttamente a **DocumentProperties** e il valore *fmode* è impostato su DM \_ in \_ buffer \| DM \_ in \_ prompt \| DM \_ out \_ buffer.</span><span class="sxs-lookup"><span data-stu-id="9f20e-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="9f20e-130">A differenza di **DocumentProperties**, questa funzione restituisce solo 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="9f20e-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="9f20e-131">Pertanto, non è possibile determinare la dimensione richiesta di [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) impostando *pDevMode* su zero.</span><span class="sxs-lookup"><span data-stu-id="9f20e-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="9f20e-132">Un'applicazione può ottenere il nome a cui punta il parametro *pDeviceName* chiamando la funzione [**GetPrinter**](getprinter.md) e quindi esaminando il membro **pPrinterName** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9f20e-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f20e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f20e-133">Requirements</span></span>



| <span data-ttu-id="9f20e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f20e-134">Requirement</span></span> | <span data-ttu-id="9f20e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9f20e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f20e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f20e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9f20e-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f20e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f20e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9f20e-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f20e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f20e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f20e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f20e-141"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f20e-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9f20e-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f20e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f20e-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f20e-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9f20e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9f20e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f20e-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9f20e-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9f20e-146">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9f20e-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9f20e-147">**AdvancedDocumentPropertiesW** (Unicode) e **AdvancedDocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9f20e-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9f20e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f20e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f20e-149">Stampa</span><span class="sxs-lookup"><span data-stu-id="9f20e-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9f20e-150">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="9f20e-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9f20e-151">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f20e-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="9f20e-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="9f20e-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="9f20e-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="9f20e-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="9f20e-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f20e-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="9f20e-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f20e-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="9f20e-156">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9f20e-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




