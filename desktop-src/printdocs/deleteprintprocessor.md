---
description: La funzione DeletePrintProcessor rimuove un processore di stampa aggiunto dalla funzione AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Funzione DeletePrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227355"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="24059-103">DeletePrintProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="24059-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="24059-104">La funzione **DeletePrintProcessor** rimuove un processore di stampa aggiunto dalla funzione [**AddPrintProcessor**](addprintprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="24059-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="24059-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24059-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="24059-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24059-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24059-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24059-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24059-108">Puntatore a una stringa con terminazione null che specifica il nome del server da cui deve essere rimosso il processore.</span><span class="sxs-lookup"><span data-stu-id="24059-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="24059-109">Se questo parametro è **null**, il processore della stampante viene rimosso localmente.</span><span class="sxs-lookup"><span data-stu-id="24059-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="24059-110">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24059-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24059-111">Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere rimosso il processore, ad esempio Windows NT x86, Windows IA64 o Windows x64.</span><span class="sxs-lookup"><span data-stu-id="24059-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="24059-112">Se questo parametro è **null**, il processore viene rimosso dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="24059-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="24059-113">Il valore consigliato è **null** perché garantisce la massima portabilità.</span><span class="sxs-lookup"><span data-stu-id="24059-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="24059-114">*pPrintProcessorName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24059-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24059-115">Puntatore a una stringa con terminazione null che specifica il nome del processore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="24059-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24059-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24059-116">Return value</span></span>

<span data-ttu-id="24059-117">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="24059-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="24059-118">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="24059-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24059-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="24059-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24059-120">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="24059-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="24059-121">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24059-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="24059-122">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="24059-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="24059-123">Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="24059-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="24059-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24059-124">Requirements</span></span>



| <span data-ttu-id="24059-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="24059-125">Requirement</span></span> | <span data-ttu-id="24059-126">Valore</span><span class="sxs-lookup"><span data-stu-id="24059-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24059-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24059-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24059-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24059-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24059-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24059-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24059-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24059-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24059-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24059-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="24059-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24059-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="24059-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="24059-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="24059-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24059-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="24059-135">DLL</span><span class="sxs-lookup"><span data-stu-id="24059-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24059-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="24059-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="24059-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="24059-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="24059-138">**DeletePrintProcessorW** (Unicode) e **DeletePrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="24059-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="24059-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24059-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24059-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="24059-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="24059-141">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="24059-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="24059-142">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="24059-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

