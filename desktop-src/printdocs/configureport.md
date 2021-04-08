---
description: La funzione ConfigurePort Visualizza la finestra di dialogo configurazione porta per una porta nel server specificato.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Funzione ConfigurePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967455"
---
# <a name="configureport-function"></a><span data-ttu-id="4b4f0-103">ConfigurePort (funzione)</span><span class="sxs-lookup"><span data-stu-id="4b4f0-103">ConfigurePort function</span></span>

<span data-ttu-id="4b4f0-104">La funzione **ConfigurePort** Visualizza la finestra di dialogo configurazione porta per una porta nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b4f0-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="4b4f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b4f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b4f0-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b4f0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4f0-108">Puntatore a una stringa con terminazione null che specifica il nome del server in cui è presente la porta specificata.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="4b4f0-109">Se questo parametro è **null**, la porta è locale.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="4b4f0-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b4f0-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4f0-111">Handle per la finestra padre della finestra di dialogo per la configurazione della porta.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4b4f0-112">*pPortName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b4f0-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b4f0-113">Puntatore a una stringa con terminazione null che specifica il nome della porta da configurare.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b4f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b4f0-114">Return value</span></span>

<span data-ttu-id="4b4f0-115">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4b4f0-116">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b4f0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b4f0-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b4f0-118">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4b4f0-119">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4b4f0-120">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4b4f0-121">Prima di chiamare la funzione **ConfigurePort** , un'applicazione deve chiamare la funzione [**EnumPorts**](enumports.md) per determinare nomi di porta validi.</span><span class="sxs-lookup"><span data-stu-id="4b4f0-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4f0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b4f0-122">Requirements</span></span>



| <span data-ttu-id="4b4f0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b4f0-123">Requirement</span></span> | <span data-ttu-id="4b4f0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4b4f0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4f0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b4f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4f0-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b4f0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b4f0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b4f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4f0-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b4f0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b4f0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b4f0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4f0-130"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b4f0-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4b4f0-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b4f0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b4f0-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b4f0-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4b4f0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4b4f0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b4f0-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4b4f0-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4b4f0-135">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4b4f0-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4b4f0-136">**ConfigurePortW** (Unicode) e **ConfigurePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4b4f0-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="4b4f0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b4f0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4f0-138">Stampa</span><span class="sxs-lookup"><span data-stu-id="4b4f0-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4b4f0-139">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4b4f0-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4b4f0-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="4b4f0-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




