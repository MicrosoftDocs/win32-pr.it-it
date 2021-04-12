---
description: La funzione DeletePrintProvidor rimuove un provider di stampa aggiunto dalla funzione AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Funzione DeletePrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232376"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="60677-103">DeletePrintProvidor (funzione)</span><span class="sxs-lookup"><span data-stu-id="60677-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="60677-104">La funzione **DeletePrintProvidor** rimuove un provider di stampa aggiunto dalla funzione [**AddPrintProvidor**](addprintprovidor.md) .</span><span class="sxs-lookup"><span data-stu-id="60677-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="60677-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60677-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="60677-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60677-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60677-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60677-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60677-108">Riservati deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="60677-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60677-109">*pEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60677-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60677-110">Puntatore a una stringa con terminazione null che specifica l'ambiente da cui deve essere rimosso il provider (ad esempio, Windows NT x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="60677-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="60677-111">Se questo parametro è **null**, il provider viene rimosso dall'ambiente corrente dell'applicazione chiamante e del computer client, non dell'applicazione di destinazione e del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="60677-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="60677-112">Il valore consigliato è **null** perché garantisce la massima portabilità.</span><span class="sxs-lookup"><span data-stu-id="60677-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="60677-113">*pPrintProviderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60677-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60677-114">Puntatore a una stringa con terminazione null che specifica il nome del provider da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="60677-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60677-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60677-115">Return value</span></span>

<span data-ttu-id="60677-116">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="60677-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="60677-117">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="60677-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="60677-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="60677-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="60677-119">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="60677-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="60677-120">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60677-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="60677-121">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="60677-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60677-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60677-122">Requirements</span></span>



| <span data-ttu-id="60677-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60677-123">Requirement</span></span> | <span data-ttu-id="60677-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60677-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60677-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60677-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60677-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60677-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60677-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60677-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60677-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60677-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60677-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60677-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60677-130"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60677-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="60677-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="60677-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="60677-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60677-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="60677-133">DLL</span><span class="sxs-lookup"><span data-stu-id="60677-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60677-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="60677-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="60677-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="60677-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="60677-136">**DeletePrintProvidorW** (Unicode) e **DeletePrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="60677-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="60677-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60677-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60677-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="60677-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="60677-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="60677-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="60677-140">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="60677-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




