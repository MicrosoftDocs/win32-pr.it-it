---
description: La funzione DeletePrinterConnection Elimina una connessione a una stampante stabilita da una chiamata a AddPrinterConnection o ConnectToPrinterDlg.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: Funzione DeletePrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317300"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="3a5dd-103">DeletePrinterConnection (funzione)</span><span class="sxs-lookup"><span data-stu-id="3a5dd-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="3a5dd-104">La funzione **DeletePrinterConnection** Elimina una connessione a una stampante stabilita da una chiamata a [**AddPrinterConnection**](addprinterconnection.md) o [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span><span class="sxs-lookup"><span data-stu-id="3a5dd-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a5dd-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="3a5dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a5dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5dd-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5dd-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5dd-108">Puntatore a una stringa con terminazione null che specifica il nome della connessione della stampante da eliminare.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5dd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a5dd-109">Return value</span></span>

<span data-ttu-id="3a5dd-110">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3a5dd-111">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5dd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a5dd-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a5dd-113">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3a5dd-114">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3a5dd-115">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3a5dd-116">La funzione **DeletePrinterConnection** non elimina i file di driver della stampante copiati nel server a cui è collegata la stampante.</span><span class="sxs-lookup"><span data-stu-id="3a5dd-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5dd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a5dd-117">Requirements</span></span>



| <span data-ttu-id="3a5dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5dd-118">Requirement</span></span> | <span data-ttu-id="3a5dd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3a5dd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5dd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5dd-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5dd-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3a5dd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5dd-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3a5dd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a5dd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a5dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5dd-125"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a5dd-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3a5dd-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a5dd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a5dd-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a5dd-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3a5dd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5dd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5dd-129"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3a5dd-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3a5dd-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3a5dd-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a5dd-131">**DeletePrinterConnectionW** (Unicode) e **DeletePrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3a5dd-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3a5dd-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a5dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5dd-133">Stampa</span><span class="sxs-lookup"><span data-stu-id="3a5dd-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3a5dd-134">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="3a5dd-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3a5dd-135">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="3a5dd-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="3a5dd-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="3a5dd-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="3a5dd-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="3a5dd-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




