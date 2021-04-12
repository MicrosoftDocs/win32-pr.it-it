---
description: La funzione DeletePort Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Funzione DeletePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232377"
---
# <a name="deleteport-function"></a><span data-ttu-id="74d0e-103">DeletePort (funzione)</span><span class="sxs-lookup"><span data-stu-id="74d0e-103">DeletePort function</span></span>

<span data-ttu-id="74d0e-104">La funzione **DeletePort** Visualizza una finestra di dialogo che consente all'utente di eliminare un nome di porta.</span><span class="sxs-lookup"><span data-stu-id="74d0e-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d0e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74d0e-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="74d0e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d0e-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d0e-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d0e-108">Puntatore a una stringa con terminazione zero che specifica il nome del server per cui la porta deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="74d0e-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="74d0e-109">Se questo parametro è **null**, viene eliminata una porta locale.</span><span class="sxs-lookup"><span data-stu-id="74d0e-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="74d0e-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d0e-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d0e-111">Handle per la finestra padre della finestra di dialogo di eliminazione della porta.</span><span class="sxs-lookup"><span data-stu-id="74d0e-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="74d0e-112">*pPortName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d0e-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d0e-113">Puntatore a una stringa con terminazione zero che specifica il nome della porta da eliminare.</span><span class="sxs-lookup"><span data-stu-id="74d0e-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d0e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74d0e-114">Return value</span></span>

<span data-ttu-id="74d0e-115">Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="74d0e-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="74d0e-116">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="74d0e-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="74d0e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="74d0e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74d0e-118">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="74d0e-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="74d0e-119">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74d0e-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="74d0e-120">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="74d0e-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="74d0e-121">Un'applicazione può recuperare i nomi delle porte valide chiamando la funzione [**EnumPorts**](enumports.md) .</span><span class="sxs-lookup"><span data-stu-id="74d0e-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="74d0e-122">La funzione **DeletePort** restituisce un errore se una stampante è attualmente connessa alla porta specificata.</span><span class="sxs-lookup"><span data-stu-id="74d0e-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="74d0e-123">Il chiamante della funzione **DeletePort** deve avere \_ accesso al server \_ per amministrare l'accesso al server a cui è connessa la porta.</span><span class="sxs-lookup"><span data-stu-id="74d0e-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d0e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74d0e-124">Requirements</span></span>



| <span data-ttu-id="74d0e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d0e-125">Requirement</span></span> | <span data-ttu-id="74d0e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="74d0e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d0e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d0e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="74d0e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d0e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74d0e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d0e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="74d0e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d0e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74d0e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74d0e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d0e-132"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74d0e-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74d0e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="74d0e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="74d0e-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d0e-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="74d0e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="74d0e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74d0e-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="74d0e-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="74d0e-137">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="74d0e-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74d0e-138">**DeletePortW** (Unicode) e **DeletePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74d0e-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="74d0e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74d0e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d0e-140">Stampa</span><span class="sxs-lookup"><span data-stu-id="74d0e-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74d0e-141">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="74d0e-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="74d0e-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="74d0e-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="74d0e-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="74d0e-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




