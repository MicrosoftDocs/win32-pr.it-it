---
description: La funzione EnumForms enumera i form supportati dalla stampante specificata.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Funzione EnumForms (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345301"
---
# <a name="enumforms-function"></a><span data-ttu-id="24bae-103">EnumForms (funzione)</span><span class="sxs-lookup"><span data-stu-id="24bae-103">EnumForms function</span></span>

<span data-ttu-id="24bae-104">La funzione **EnumForms** enumera i form supportati dalla stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="24bae-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="24bae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24bae-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="24bae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24bae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24bae-107">*hPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24bae-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-108">Handle per la stampante per cui è necessario enumerare i moduli.</span><span class="sxs-lookup"><span data-stu-id="24bae-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="24bae-109">Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.</span><span class="sxs-lookup"><span data-stu-id="24bae-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="24bae-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="24bae-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-111">Specifica la versione della struttura a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="24bae-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="24bae-112">Questo valore deve essere 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="24bae-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="24bae-113">*pForm* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24bae-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-114">Puntatore a una o più [**strutture \_ info form \_ 1**](form-info-1.md) o a una o più [**strutture \_ info form \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="24bae-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="24bae-115">Tutte le strutture avranno lo stesso livello.</span><span class="sxs-lookup"><span data-stu-id="24bae-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="24bae-116">*cbBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24bae-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-117">Specifica la dimensione, in byte, del buffer a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="24bae-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="24bae-118">*pcbNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24bae-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-119">Puntatore a una variabile che riceve il numero di byte copiati nella matrice a cui punta *pForm* (se l'operazione ha esito positivo) o il numero di byte richiesti (in caso di esito negativo perché *cbBuf* è troppo piccolo).</span><span class="sxs-lookup"><span data-stu-id="24bae-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="24bae-120">*pcReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24bae-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24bae-121">Puntatore a una variabile che riceve il numero di strutture copiate nella matrice a cui punta *pForm* .</span><span class="sxs-lookup"><span data-stu-id="24bae-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24bae-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24bae-122">Return value</span></span>

<span data-ttu-id="24bae-123">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="24bae-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="24bae-124">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="24bae-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24bae-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="24bae-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24bae-126">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="24bae-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="24bae-127">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24bae-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="24bae-128">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="24bae-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="24bae-129">Se il chiamante è remoto e il *livello* è 2, il valore **StringType** delle strutture [**\_ info \_ 2 del modulo**](form-info-2.md) restituite sarà sempre di tipo **stringa \_ LANGPAIR**.</span><span class="sxs-lookup"><span data-stu-id="24bae-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="24bae-130">In Windows Vista, i dati del modulo restituiti da **EnumForms** vengono recuperati da una cache locale quando *hPrinter* fa riferimento a un server di stampa remoto o a una stampante ospitata da un server di stampa ed è presente almeno una connessione aperta a una stampante nel server di stampa remoto.</span><span class="sxs-lookup"><span data-stu-id="24bae-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="24bae-131">In tutte le altre configurazioni, viene eseguita una query sui dati del modulo dal server di stampa remoto.</span><span class="sxs-lookup"><span data-stu-id="24bae-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bae-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24bae-132">Requirements</span></span>



| <span data-ttu-id="24bae-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="24bae-133">Requirement</span></span> | <span data-ttu-id="24bae-134">Valore</span><span class="sxs-lookup"><span data-stu-id="24bae-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24bae-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24bae-135">Minimum supported client</span></span><br/> | <span data-ttu-id="24bae-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24bae-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24bae-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24bae-137">Minimum supported server</span></span><br/> | <span data-ttu-id="24bae-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24bae-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24bae-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24bae-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="24bae-140"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24bae-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="24bae-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="24bae-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="24bae-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24bae-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="24bae-143">DLL</span><span class="sxs-lookup"><span data-stu-id="24bae-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24bae-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="24bae-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="24bae-145">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="24bae-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="24bae-146">**EnumFormsW** (Unicode) e **EnumFormsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24bae-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="24bae-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24bae-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24bae-148">Stampa</span><span class="sxs-lookup"><span data-stu-id="24bae-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="24bae-149">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="24bae-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="24bae-150">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="24bae-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="24bae-151">**Informazioni sul modulo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="24bae-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="24bae-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="24bae-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




