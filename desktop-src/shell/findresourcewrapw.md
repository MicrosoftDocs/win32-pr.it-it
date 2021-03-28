---
description: Determina il percorso di una risorsa con il tipo e il nome specificati nel modulo specificato.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227452"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="193ed-103">FindResourceWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="193ed-103">FindResourceWrapW function</span></span>

<span data-ttu-id="193ed-104">\[**FindResourceWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="193ed-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="193ed-105">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="193ed-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="193ed-106">Usare invece [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]</span><span class="sxs-lookup"><span data-stu-id="193ed-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="193ed-107">Determina il percorso di una risorsa con il tipo e il nome specificati nel modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="193ed-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="193ed-108">**FindResourceWrapW** è un wrapper per la funzione **FindResourceW** .</span><span class="sxs-lookup"><span data-stu-id="193ed-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="193ed-109">Per ulteriori note sull'utilizzo, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="193ed-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="193ed-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="193ed-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="193ed-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="193ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193ed-112">*hmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193ed-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193ed-113">Tipo: **hmodule**</span><span class="sxs-lookup"><span data-stu-id="193ed-113">Type: **HMODULE**</span></span>

<span data-ttu-id="193ed-114">Handle per il modulo il cui file eseguibile contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="193ed-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="193ed-115">Il valore **null** specifica l'handle del modulo associato al file di immagine utilizzato dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="193ed-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="193ed-116">*lpName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193ed-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193ed-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="193ed-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="193ed-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="193ed-118">The name of the resource.</span></span> <span data-ttu-id="193ed-119">Per ulteriori informazioni, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="193ed-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="193ed-120">*lpType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="193ed-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193ed-121">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="193ed-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="193ed-122">Puntatore a una stringa che specifica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="193ed-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="193ed-123">Per ulteriori informazioni, vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="193ed-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193ed-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="193ed-124">Return value</span></span>

<span data-ttu-id="193ed-125">Tipo: **HRSRC**</span><span class="sxs-lookup"><span data-stu-id="193ed-125">Type: **HRSRC**</span></span>

<span data-ttu-id="193ed-126">Se la funzione ha esito positivo, il valore restituito è un handle per il blocco di informazioni della risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="193ed-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="193ed-127">Per ottenere un handle per la risorsa, passare questo handle alla funzione [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="193ed-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="193ed-128">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="193ed-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="193ed-129">Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="193ed-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="193ed-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="193ed-130">Remarks</span></span>

<span data-ttu-id="193ed-131">Se è necessario specificare una particolare localizzazione, utilizzare la funzione [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) anziché **FindResourceWrapW**.</span><span class="sxs-lookup"><span data-stu-id="193ed-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="193ed-132">**FindResourceWrapW** offre la possibilità di usare stringhe Unicode nei sistemi operativi precedenti.</span><span class="sxs-lookup"><span data-stu-id="193ed-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="193ed-133">Il metodo preferito consiste nell'usare [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="193ed-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="193ed-134">**FindResourceWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 66.</span><span class="sxs-lookup"><span data-stu-id="193ed-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="193ed-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="193ed-135">Requirements</span></span>



| <span data-ttu-id="193ed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="193ed-136">Requirement</span></span> | <span data-ttu-id="193ed-137">Valore</span><span class="sxs-lookup"><span data-stu-id="193ed-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="193ed-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="193ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="193ed-139">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="193ed-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="193ed-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="193ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="193ed-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="193ed-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="193ed-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="193ed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="193ed-143"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="193ed-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="193ed-144">DLL</span><span class="sxs-lookup"><span data-stu-id="193ed-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="193ed-145"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="193ed-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="193ed-146">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="193ed-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="193ed-147">**FindResourceWrapW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="193ed-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="193ed-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="193ed-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193ed-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="193ed-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
