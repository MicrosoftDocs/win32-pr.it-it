---
description: La funzione AddForm aggiunge un modulo all'elenco dei moduli disponibili che è possibile selezionare per la stampante specificata.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Funzione AddForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311570"
---
# <a name="addform-function"></a><span data-ttu-id="c55e2-103">AddForm (funzione)</span><span class="sxs-lookup"><span data-stu-id="c55e2-103">AddForm function</span></span>

<span data-ttu-id="c55e2-104">La funzione **AddForm** aggiunge un modulo all'elenco dei moduli disponibili che è possibile selezionare per la stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="c55e2-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c55e2-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="c55e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c55e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55e2-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c55e2-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55e2-108">Handle per la stampante che supporta la stampa con il form specificato.</span><span class="sxs-lookup"><span data-stu-id="c55e2-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="c55e2-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="c55e2-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c55e2-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c55e2-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55e2-111">Livello della struttura a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="c55e2-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="c55e2-112">Questo valore deve essere 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c55e2-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c55e2-113">*pForm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c55e2-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c55e2-114">Puntatore a una struttura [**di \_ informazioni \_ su form 1**](form-info-1.md) o [**form \_ info \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c55e2-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55e2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c55e2-115">Return value</span></span>

<span data-ttu-id="c55e2-116">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c55e2-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c55e2-117">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c55e2-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55e2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c55e2-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c55e2-119">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c55e2-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c55e2-120">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c55e2-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c55e2-121">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="c55e2-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c55e2-122">Un'applicazione può determinare quali moduli sono disponibili per una stampante chiamando la funzione [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="c55e2-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="c55e2-123">Se *pForm* punta a un [**modulo \_ info \_ 2**](form-info-2.md), **AddForm** avrà esito negativo se un modulo con il nome specificato esiste già o se il valore *pKeyword* della struttura esiste già.</span><span class="sxs-lookup"><span data-stu-id="c55e2-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55e2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c55e2-124">Requirements</span></span>



| <span data-ttu-id="c55e2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55e2-125">Requirement</span></span> | <span data-ttu-id="c55e2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c55e2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55e2-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c55e2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c55e2-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c55e2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c55e2-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c55e2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c55e2-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c55e2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c55e2-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c55e2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c55e2-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c55e2-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c55e2-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="c55e2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c55e2-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c55e2-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c55e2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c55e2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c55e2-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c55e2-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c55e2-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c55e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55e2-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="c55e2-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c55e2-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="c55e2-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c55e2-140">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="c55e2-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="c55e2-141">**Informazioni sul modulo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c55e2-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="c55e2-142">**Informazioni sul modulo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c55e2-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="c55e2-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c55e2-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




