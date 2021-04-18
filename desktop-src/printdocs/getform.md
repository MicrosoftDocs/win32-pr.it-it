---
description: La funzione GetForm recupera le informazioni relative a un modulo specificato.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Funzione GetForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314016"
---
# <a name="getform-function"></a><span data-ttu-id="4fbb5-103">Funzione GetForm</span><span class="sxs-lookup"><span data-stu-id="4fbb5-103">GetForm function</span></span>

<span data-ttu-id="4fbb5-104">La funzione **GetForm** recupera le informazioni relative a un modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fbb5-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4fbb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fbb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fbb5-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-108">Handle per la stampante.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-108">A handle to the printer.</span></span> <span data-ttu-id="4fbb5-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb5-110">*pFormName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-111">Puntatore a una stringa con terminazione null che specifica il nome del form.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="4fbb5-112">Per ottenere i nomi dei form supportati dalla stampante, chiamare la funzione [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbb5-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb5-113">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-114">Versione della struttura a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="4fbb5-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="4fbb5-115">Questo valore deve essere 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb5-116">*pForm* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-117">Puntatore a una matrice di byte che riceve il [**form inizializzato \_ informazioni \_ 1**](form-info-1.md) o la struttura di [**informazioni sul form \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbb5-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb5-118">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-119">Dimensione, in byte, della matrice *pForm* .</span><span class="sxs-lookup"><span data-stu-id="4fbb5-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb5-120">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb5-121">Puntatore a un valore che specifica il numero di byte copiati se la funzione ha esito positivo o il numero di byte necessari se *cbBuf* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fbb5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fbb5-122">Return value</span></span>

<span data-ttu-id="4fbb5-123">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4fbb5-124">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbb5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fbb5-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4fbb5-126">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4fbb5-127">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4fbb5-128">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4fbb5-129">Se il chiamante è remoto e il *livello* è 2, il valore di **StringType** del modulo restituito [**\_ info \_ 2**](form-info-2.md) sarà sempre stringa \_ LANGPAIR.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbb5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fbb5-130">Requirements</span></span>



| <span data-ttu-id="4fbb5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fbb5-131">Requirement</span></span> | <span data-ttu-id="4fbb5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4fbb5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbb5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fbb5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbb5-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4fbb5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fbb5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbb5-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fbb5-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4fbb5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fbb5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fbb5-138"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb5-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4fbb5-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="4fbb5-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fbb5-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb5-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4fbb5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4fbb5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fbb5-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb5-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4fbb5-143">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4fbb5-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4fbb5-144">**GetFormW** (Unicode) e **getforma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4fbb5-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="4fbb5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fbb5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbb5-146">Stampa</span><span class="sxs-lookup"><span data-stu-id="4fbb5-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4fbb5-147">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4fbb5-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4fbb5-148">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="4fbb5-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="4fbb5-149">**DeleteForm**</span><span class="sxs-lookup"><span data-stu-id="4fbb5-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="4fbb5-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4fbb5-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4fbb5-151">**Diformi**</span><span class="sxs-lookup"><span data-stu-id="4fbb5-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




