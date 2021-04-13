---
description: La funzione seform imposta le informazioni sul form per la stampante specificata.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Funzione seform (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345281"
---
# <a name="setform-function"></a><span data-ttu-id="fa343-103">Funzione seform</span><span class="sxs-lookup"><span data-stu-id="fa343-103">SetForm function</span></span>

<span data-ttu-id="fa343-104">La funzione **seform** imposta le informazioni sul form per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="fa343-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa343-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa343-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="fa343-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa343-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa343-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa343-108">Handle per la stampante per cui sono impostate le informazioni sul form.</span><span class="sxs-lookup"><span data-stu-id="fa343-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="fa343-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="fa343-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="fa343-110">*pFormName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa343-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa343-111">Puntatore a una stringa con terminazione null che specifica il nome del modulo per il quale sono impostate le informazioni sul form.</span><span class="sxs-lookup"><span data-stu-id="fa343-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="fa343-112">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fa343-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa343-113">Versione della struttura a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="fa343-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="fa343-114">Questo valore deve essere 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="fa343-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fa343-115">*pForm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa343-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa343-116">Puntatore a una struttura [**di \_ informazioni \_ su form 1**](form-info-1.md) o [**form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="fa343-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa343-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa343-117">Return value</span></span>

<span data-ttu-id="fa343-118">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fa343-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fa343-119">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="fa343-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa343-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa343-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa343-121">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="fa343-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fa343-122">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fa343-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fa343-123">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="fa343-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fa343-124">È **possibile chiamare** il metodo più volte per un'informazione sul [**form esistente \_ \_ 2**](form-info-2.md), ogni chiamata che aggiunge altre coppie di valori **pDisplayName** e **wLangId** .</span><span class="sxs-lookup"><span data-stu-id="fa343-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="fa343-125">Tutte le versioni dei linguaggi del modulo otterranno i valori **size** e **ImageableArea** del **form \_ info \_ 2** nella chiamata più recente a **seform**.</span><span class="sxs-lookup"><span data-stu-id="fa343-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="fa343-126">Se il chiamante è remoto e il *livello* è 2, il valore di **StringType** nel [**formato \_ info \_ 2**](form-info-2.md) non può essere \_ MUIDLL di stringa.</span><span class="sxs-lookup"><span data-stu-id="fa343-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa343-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa343-127">Requirements</span></span>



| <span data-ttu-id="fa343-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa343-128">Requirement</span></span> | <span data-ttu-id="fa343-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fa343-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa343-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa343-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fa343-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa343-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa343-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa343-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fa343-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa343-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa343-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa343-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa343-135"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa343-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fa343-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa343-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa343-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa343-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fa343-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fa343-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa343-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="fa343-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="fa343-140">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="fa343-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa343-141">**SetFormW** (Unicode) e **seforma** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fa343-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="fa343-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa343-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa343-143">Stampa</span><span class="sxs-lookup"><span data-stu-id="fa343-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fa343-144">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="fa343-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fa343-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="fa343-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="fa343-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fa343-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="fa343-147">**Informazioni sul modulo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fa343-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="fa343-148">**Informazioni sul modulo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fa343-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




