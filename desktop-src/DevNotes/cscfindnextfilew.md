---
description: Continua un'operazione di ricerca di file.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: CSCFindNextFileW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328855"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="fc8ba-103">CSCFindNextFileW (funzione)</span><span class="sxs-lookup"><span data-stu-id="fc8ba-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="fc8ba-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="fc8ba-105">Continua un'operazione di ricerca di file.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8ba-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc8ba-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="fc8ba-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc8ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8ba-108">*hFind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-109">Handle di ricerca restituito dalla funzione [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="fc8ba-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ba-110">*lpFind32* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-111">Puntatore alla struttura di [**\_ \_ dati Find Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) che riceve informazioni sul file o sulla sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ba-112">*lpdwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-113">Codice NTSTATUS che indica lo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ba-114">*lpdwPinCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-115">Questo parametro è diverso da zero se il file è stato reso disponibile offline o 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fc8ba-116">*lpdwHintFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-117">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fc8ba-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fc8ba-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="fc8ba-119">Significato</span><span class="sxs-lookup"><span data-stu-id="fc8ba-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="fc8ba-120"><dt>**Flag \_ di 0x01 \_ \_ \_ utente pin hint CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fc8ba-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="fc8ba-121">Un utente ha reso disponibile il file offline.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="fc8ba-122"><dt>**Flag \_ di Il \_ \_ pin dell'hint CSC \_ eredita l' \_ utente**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ba-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="fc8ba-123">Un utente ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="fc8ba-124"><dt>**Flag \_ di Il \_ pin dell'hint CSC \_ eredita il \_ \_ sistema**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ba-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="fc8ba-125">Un amministratore o un criterio di gruppo ha reso l'elemento padre disponibile offline e contrassegnato come padre in modo che i relativi elementi figlio siano disponibili offline.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="fc8ba-126"><dt>**Flag \_ di 0x10 \_ \_ \_ sistema pin hint CSC**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fc8ba-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="fc8ba-127">Un amministratore o un criterio di gruppo ha reso disponibile il file offline.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="fc8ba-128">*lpOrgFileTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc8ba-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8ba-129">Puntatore a una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) per ricevere le informazioni sulla data e l'ora per il file o la sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8ba-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc8ba-130">Return value</span></span>

<span data-ttu-id="fc8ba-131">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8ba-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc8ba-132">Remarks</span></span>

<span data-ttu-id="fc8ba-133">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fc8ba-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8ba-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc8ba-134">Requirements</span></span>



| <span data-ttu-id="fc8ba-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8ba-135">Requirement</span></span> | <span data-ttu-id="fc8ba-136">Valore</span><span class="sxs-lookup"><span data-stu-id="fc8ba-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ba-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fc8ba-137">DLL</span></span><br/> | <dl> <span data-ttu-id="fc8ba-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8ba-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
