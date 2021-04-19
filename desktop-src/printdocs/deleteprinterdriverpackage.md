---
description: Elimina un pacchetto di driver della stampante dall'archivio driver.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Funzione DeletePrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311548"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="3308f-103">DeletePrinterDriverPackage (funzione)</span><span class="sxs-lookup"><span data-stu-id="3308f-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="3308f-104">Elimina un pacchetto di driver della stampante dall'archivio driver.</span><span class="sxs-lookup"><span data-stu-id="3308f-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3308f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3308f-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="3308f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3308f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3308f-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3308f-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3308f-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa da cui viene eliminato il pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="3308f-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="3308f-109">Un valore di puntatore **null** indica il computer locale.</span><span class="sxs-lookup"><span data-stu-id="3308f-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="3308f-110">*pszInfPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3308f-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3308f-111">Puntatore a una stringa costante a terminazione null che specifica il percorso del \* file. inf del driver.</span><span class="sxs-lookup"><span data-stu-id="3308f-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="3308f-112">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3308f-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3308f-113">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86.</span><span class="sxs-lookup"><span data-stu-id="3308f-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="3308f-114">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3308f-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3308f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3308f-115">Return value</span></span>

<span data-ttu-id="3308f-116">S \_ OK, se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3308f-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="3308f-117">E \_ AccessDenied, se il pacchetto è stato fornito con Windows.</span><span class="sxs-lookup"><span data-stu-id="3308f-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="3308f-118">\_Codice HRESULT ( \_ \_ \_ pacchetto driver di stampa \_ di errore in \_ uso), se il pacchetto viene usato.</span><span class="sxs-lookup"><span data-stu-id="3308f-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="3308f-119">In caso contrario, **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="3308f-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="3308f-120">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="3308f-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3308f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3308f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3308f-122">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3308f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3308f-123">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3308f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3308f-124">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="3308f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3308f-125">L'archivio driver è in genere% windir% \\ inf o% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="3308f-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="3308f-126">Non è possibile rimuovere con questa funzione un pacchetto driver fornito con Windows.</span><span class="sxs-lookup"><span data-stu-id="3308f-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="3308f-127">L'utente deve disporre dei privilegi di amministrazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="3308f-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="3308f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3308f-128">Requirements</span></span>



| <span data-ttu-id="3308f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3308f-129">Requirement</span></span> | <span data-ttu-id="3308f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3308f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3308f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3308f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3308f-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3308f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3308f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3308f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3308f-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3308f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3308f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3308f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3308f-136"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3308f-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3308f-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="3308f-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3308f-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3308f-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3308f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3308f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3308f-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3308f-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="3308f-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3308f-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3308f-142">**DeletePrinterDriverPackageW** (Unicode) e **DeletePrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3308f-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3308f-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3308f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3308f-144">Stampa</span><span class="sxs-lookup"><span data-stu-id="3308f-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3308f-145">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="3308f-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

