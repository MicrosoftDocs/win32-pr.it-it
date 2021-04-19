---
description: La funzione AddPrintProvidor installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Funzione AddPrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311564"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="cb846-103">AddPrintProvidor (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb846-103">AddPrintProvidor function</span></span>

<span data-ttu-id="cb846-104">La funzione **AddPrintProvidor** installa un provider di stampa locale e collega i file di configurazione, i dati e il provider.</span><span class="sxs-lookup"><span data-stu-id="cb846-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb846-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb846-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cb846-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb846-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb846-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb846-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installato il provider.</span><span class="sxs-lookup"><span data-stu-id="cb846-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="cb846-109">Per i sistemi che supportano solo l'installazione locale di provider, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="cb846-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cb846-110">*Livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cb846-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb846-111">Livello della struttura a cui punta *pProviderInfo* .</span><span class="sxs-lookup"><span data-stu-id="cb846-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="cb846-112">Può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="cb846-112">It can be one of the following.</span></span>



| <span data-ttu-id="cb846-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cb846-113">Value</span></span>                                                                                                | <span data-ttu-id="cb846-114">Significato</span><span class="sxs-lookup"><span data-stu-id="cb846-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="cb846-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cb846-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cb846-116">La funzione usa una struttura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="cb846-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="cb846-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cb846-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cb846-118">La funzione usa una struttura [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="cb846-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cb846-119">*pProviderInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb846-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb846-120">Puntatore a una struttura di provider di stampa, come indicato dal *livello*.</span><span class="sxs-lookup"><span data-stu-id="cb846-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb846-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb846-121">Return value</span></span>

<span data-ttu-id="cb846-122">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cb846-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="cb846-123">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="cb846-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb846-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb846-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb846-125">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="cb846-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="cb846-126">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb846-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="cb846-127">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="cb846-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="cb846-128">Prima che un'applicazione chiami la funzione **AddPrintProvidor** , tutti i file richiesti dal provider devono essere copiati nella directory system32.</span><span class="sxs-lookup"><span data-stu-id="cb846-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="cb846-129">Un provider aggiunto da **AddPrintProvidor** può essere rimosso chiamando [**DeletePrintProvidor**](deleteprintprovidor.md).</span><span class="sxs-lookup"><span data-stu-id="cb846-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb846-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb846-130">Requirements</span></span>



| <span data-ttu-id="cb846-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb846-131">Requirement</span></span> | <span data-ttu-id="cb846-132">Valore</span><span class="sxs-lookup"><span data-stu-id="cb846-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb846-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb846-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cb846-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb846-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb846-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb846-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cb846-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb846-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb846-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb846-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb846-138"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb846-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb846-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb846-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb846-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb846-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="cb846-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cb846-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb846-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="cb846-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="cb846-143">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cb846-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb846-144">**AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb846-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="cb846-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb846-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb846-146">Stampa</span><span class="sxs-lookup"><span data-stu-id="cb846-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cb846-147">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="cb846-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="cb846-148">**DeletePrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="cb846-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="cb846-149">**PROVIDOR \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="cb846-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="cb846-150">**PROVIDOR \_ info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="cb846-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




