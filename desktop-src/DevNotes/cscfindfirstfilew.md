---
description: Cerca un file nella cache File offline che soddisfi i criteri specificati.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331198"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="edf4d-103">CSCFindFirstFileW (funzione)</span><span class="sxs-lookup"><span data-stu-id="edf4d-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="edf4d-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="edf4d-105">Cerca un file nella cache File offline che soddisfi i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="edf4d-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf4d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edf4d-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="edf4d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="edf4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edf4d-108">*lpszFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-109">Puntatore a una stringa con terminazione null che specifica una directory o un percorso UNC valido.</span><span class="sxs-lookup"><span data-stu-id="edf4d-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="edf4d-110">*lpFind32* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-111">Puntatore alla struttura di [**\_ \_ dati Find Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) che riceve informazioni sul file o sulla sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="edf4d-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="edf4d-112">*lpdwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-113">Codice NTSTATUS che indica lo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="edf4d-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="edf4d-114">*lpdwPinCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-115">Questo parametro è diverso da zero se il file è stato reso disponibile offline o 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="edf4d-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="edf4d-116">*lpdwHintFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-117">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="edf4d-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="edf4d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="edf4d-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="edf4d-119">Significato</span><span class="sxs-lookup"><span data-stu-id="edf4d-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="edf4d-120"><dt>**Flag \_ di 0x01 \_ \_ \_ utente pin hint CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="edf4d-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="edf4d-121">Un utente ha reso disponibile il file offline.</span><span class="sxs-lookup"><span data-stu-id="edf4d-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="edf4d-122"><dt>**Flag \_ di Il \_ \_ pin dell'hint CSC \_ eredita l' \_ utente**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="edf4d-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="edf4d-123">Un utente ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.</span><span class="sxs-lookup"><span data-stu-id="edf4d-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="edf4d-124"><dt>**Flag \_ di Il \_ pin dell'hint CSC \_ eredita il \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="edf4d-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="edf4d-125">Un amministratore o un criterio di gruppo ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.</span><span class="sxs-lookup"><span data-stu-id="edf4d-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="edf4d-126"><dt>**Flag \_ di 0x10 \_ \_ \_ sistema pin hint CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="edf4d-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="edf4d-127">Un amministratore o un criterio di gruppo ha reso disponibile il file offline.</span><span class="sxs-lookup"><span data-stu-id="edf4d-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="edf4d-128">*lpOrgFileTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edf4d-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edf4d-129">Puntatore a una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per ricevere le informazioni sulla data e l'ora per il file o la sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="edf4d-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edf4d-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edf4d-130">Return value</span></span>

<span data-ttu-id="edf4d-131">Se la funzione ha esito positivo, il valore restituito è un handle di ricerca usato in una chiamata successiva a [**CSCFindNextFileW**](cscfindnextfilew.md) o [**CSCFindClose**](cscfindclose.md).</span><span class="sxs-lookup"><span data-stu-id="edf4d-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="edf4d-132">Se la funzione ha esito negativo, il valore restituito è **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="edf4d-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="edf4d-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="edf4d-133">Remarks</span></span>

<span data-ttu-id="edf4d-134">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="edf4d-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf4d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edf4d-135">Requirements</span></span>



| <span data-ttu-id="edf4d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="edf4d-136">Requirement</span></span> | <span data-ttu-id="edf4d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="edf4d-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edf4d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="edf4d-138">DLL</span></span><br/> | <dl> <span data-ttu-id="edf4d-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf4d-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
