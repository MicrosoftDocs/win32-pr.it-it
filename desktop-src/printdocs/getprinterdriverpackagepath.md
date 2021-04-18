---
description: Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Funzione GetPrinterDriverPackagePath (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318380"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="44efc-103">GetPrinterDriverPackagePath (funzione)</span><span class="sxs-lookup"><span data-stu-id="44efc-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="44efc-104">Recupera il percorso del pacchetto di driver della stampante specificato in un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="44efc-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="44efc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44efc-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="44efc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44efc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44efc-107">*pszServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44efc-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-108">Puntatore a una stringa costante a terminazione null che specifica il nome del server di stampa.</span><span class="sxs-lookup"><span data-stu-id="44efc-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="44efc-109">Utilizzare **null** per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="44efc-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-110">*pszEnvironment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44efc-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-111">Puntatore a una stringa costante a terminazione null che specifica l'architettura del processore, ad esempio Windows NT x86.</span><span class="sxs-lookup"><span data-stu-id="44efc-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="44efc-112">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="44efc-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-113">*pszLanguage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44efc-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-114">Puntatore a una stringa costante a terminazione null che specifica la lingua dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) per il driver da installare.</span><span class="sxs-lookup"><span data-stu-id="44efc-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="44efc-115">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="44efc-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-116">*pszPackageID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44efc-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-117">Puntatore a una stringa costante a terminazione null che specifica l'ID del pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="44efc-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-118">*pszDriverPackageCab* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="44efc-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-119">Puntatore a una stringa con terminazione null che specifica il percorso del file CAB per il pacchetto driver.</span><span class="sxs-lookup"><span data-stu-id="44efc-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="44efc-120">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="44efc-120">This can be **NULL**.</span></span> <span data-ttu-id="44efc-121">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="44efc-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-122">*cchDriverPackageCab* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44efc-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-123">Dimensione, in caratteri, del buffer *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="44efc-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="44efc-124">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="44efc-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44efc-125">*pcchRequiredSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="44efc-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44efc-126">Puntatore alla dimensione richiesta del buffer *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="44efc-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44efc-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44efc-127">Return value</span></span>

<span data-ttu-id="44efc-128">Se l'operazione ha esito positivo, il valore restituito è \_ OK, altrimenti **HRESULT** conterrà un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="44efc-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="44efc-129">Per ulteriori informazioni sui codici di errore COM, vedere [gestione degli errori](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="44efc-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44efc-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="44efc-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44efc-131">Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="44efc-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="44efc-132">La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44efc-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="44efc-133">La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.</span><span class="sxs-lookup"><span data-stu-id="44efc-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="44efc-134">Per ottenere un valore per *cchDriverPackageCab*, chiamare la funzione con **null** come valore di *pszDriverPackageCab*.</span><span class="sxs-lookup"><span data-stu-id="44efc-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="44efc-135">Usare il valore restituito in *pcchRequiredSize* come valore di *cchDriverPackageCab* e chiamare di nuovo la funzione.</span><span class="sxs-lookup"><span data-stu-id="44efc-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="44efc-136">*PszPackageID* viene in genere ottenuto da una chiamata a [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span><span class="sxs-lookup"><span data-stu-id="44efc-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44efc-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44efc-137">Requirements</span></span>



| <span data-ttu-id="44efc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="44efc-138">Requirement</span></span> | <span data-ttu-id="44efc-139">Valore</span><span class="sxs-lookup"><span data-stu-id="44efc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44efc-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44efc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="44efc-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44efc-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="44efc-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44efc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="44efc-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44efc-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="44efc-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44efc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="44efc-145"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44efc-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="44efc-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="44efc-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="44efc-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44efc-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="44efc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="44efc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44efc-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44efc-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="44efc-150">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="44efc-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="44efc-151">**GetPrinterDriverPackagePathW** (Unicode) e **GetPrinterDriverPackagePathA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="44efc-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="44efc-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44efc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44efc-153">Stampa</span><span class="sxs-lookup"><span data-stu-id="44efc-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="44efc-154">Funzioni dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="44efc-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

