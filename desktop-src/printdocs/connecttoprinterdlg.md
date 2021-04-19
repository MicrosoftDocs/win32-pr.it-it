---
description: La funzione ConnectToPrinterDlg Visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Funzione ConnectToPrinterDlg (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318036"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="8e7f4-103">ConnectToPrinterDlg (funzione)</span><span class="sxs-lookup"><span data-stu-id="8e7f4-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="8e7f4-104">La funzione **ConnectToPrinterDlg** Visualizza una finestra di dialogo che consente agli utenti di esplorare e connettersi alle stampanti in una rete.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="8e7f4-105">Se l'utente seleziona una stampante, la funzione tenta di crearvi una connessione. Se nel server non è installato un driver idoneo, all'utente viene offerta la possibilità di creare una stampante localmente.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e7f4-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8e7f4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e7f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e7f4-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e7f4-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e7f4-109">Specifica la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8e7f4-110">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e7f4-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e7f4-111">Questo parametro è riservato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e7f4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e7f4-112">Return value</span></span>

<span data-ttu-id="8e7f4-113">Se la funzione ha esito positivo e l'utente seleziona una stampante, il valore restituito è un handle per la stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="8e7f4-114">Se la funzione ha esito negativo o se l'utente annulla la finestra di dialogo senza selezionare una stampante, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e7f4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e7f4-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8e7f4-116">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8e7f4-117">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8e7f4-118">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8e7f4-119">La funzione **ConnectToPrinterDlg** tenta di creare una connessione alla stampante selezionata.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="8e7f4-120">Tuttavia, se il server in cui risiede la stampante non dispone di un driver idoneo, la funzione offre all'utente la possibilità di creare una stampante localmente.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="8e7f4-121">Un'applicazione chiamante è in grado di determinare se la funzione ha creato localmente una stampante chiamando [**GetPrinter**](getprinter.md) con una struttura di [**\_ info \_ 2 della stampante**](printer-info-2.md) , quindi esaminando il membro degli **attributi** della struttura.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="8e7f4-122">Per eliminare una stampante locale, un'applicazione deve chiamare [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="8e7f4-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="8e7f4-123">Un'applicazione deve chiamare [**DeletePrinterConnection**](deleteprinterconnection.md) per eliminare una connessione a una stampante.</span><span class="sxs-lookup"><span data-stu-id="8e7f4-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e7f4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e7f4-124">Requirements</span></span>



| <span data-ttu-id="8e7f4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e7f4-125">Requirement</span></span> | <span data-ttu-id="8e7f4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8e7f4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7f4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e7f4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7f4-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e7f4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8e7f4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e7f4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7f4-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e7f4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8e7f4-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e7f4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e7f4-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e7f4-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8e7f4-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e7f4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e7f4-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e7f4-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8e7f4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8e7f4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e7f4-136"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8e7f4-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="8e7f4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e7f4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7f4-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="8e7f4-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="8e7f4-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-140">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-142">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-143">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-144">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="8e7f4-145">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8e7f4-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




