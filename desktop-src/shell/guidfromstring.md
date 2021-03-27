---
description: Converte una stringa in un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881582"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="d1c86-103">GUIDFromString (funzione)</span><span class="sxs-lookup"><span data-stu-id="d1c86-103">GUIDFromString function</span></span>

<span data-ttu-id="d1c86-104">\[**GUIDFromString** è disponibile tramite Windows XP con Service Pack 2 (SP2) o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1c86-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="d1c86-105">Potrebbe essere modificato o non disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d1c86-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d1c86-106">Le applicazioni devono utilizzare [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) o [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) al posto di questa funzione.\]</span><span class="sxs-lookup"><span data-stu-id="d1c86-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="d1c86-107">Converte una stringa in un GUID.</span><span class="sxs-lookup"><span data-stu-id="d1c86-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c86-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1c86-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="d1c86-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1c86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c86-110">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1c86-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c86-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="d1c86-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="d1c86-112">Puntatore alla stringa con terminazione null da convertire.</span><span class="sxs-lookup"><span data-stu-id="d1c86-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="d1c86-113">Il formato della stringa deve essere il seguente:</span><span class="sxs-lookup"><span data-stu-id="d1c86-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="d1c86-114">*pguid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1c86-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c86-115">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="d1c86-115">Type: **LPGUID**</span></span>

<span data-ttu-id="d1c86-116">Puntatore a un buffer per ricevere il GUID quando il metodo restituisce un risultato.</span><span class="sxs-lookup"><span data-stu-id="d1c86-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c86-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1c86-117">Return value</span></span>

<span data-ttu-id="d1c86-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="d1c86-118">Type: **BOOL**</span></span>

<span data-ttu-id="d1c86-119">**True** se il GUID è stato creato correttamente; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d1c86-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c86-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1c86-120">Remarks</span></span>

<span data-ttu-id="d1c86-121">Questa funzione non è dichiarata in un'intestazione o esportata in base al nome da un file con estensione dll.</span><span class="sxs-lookup"><span data-stu-id="d1c86-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="d1c86-122">Deve essere caricata da Shell32.dll come ordinale 703 per **GUIDFromStringA** e ordinale 704 per **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="d1c86-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="d1c86-123">È anche possibile accedervi da Shlwapi.dll come ordinale 269 per **GUIDFromStringA** e ordinale 270 per **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="d1c86-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c86-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1c86-124">Requirements</span></span>



| <span data-ttu-id="d1c86-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1c86-125">Requirement</span></span> | <span data-ttu-id="d1c86-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d1c86-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c86-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c86-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c86-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d1c86-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d1c86-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1c86-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c86-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1c86-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d1c86-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c86-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c86-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c86-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1c86-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d1c86-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1c86-134">**GUIDFromStringW** (Unicode) e **GUIDFromStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d1c86-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
