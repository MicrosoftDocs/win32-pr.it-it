---
description: Determina se un carattere è un carattere alfabetico o numerico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978122"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="44559-103">IsCharAlphaNumericWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="44559-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="44559-104">\[**IsCharAlphaNumericWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44559-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="44559-105">Non sarà disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="44559-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="44559-106">È consigliabile usare [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="44559-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="44559-107">Determina se un carattere è un carattere alfabetico o numerico.</span><span class="sxs-lookup"><span data-stu-id="44559-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="44559-108">Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="44559-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="44559-109">**IsCharAlphaNumericWrapW** è un wrapper per la funzione **IsCharAlphaNumericW** .</span><span class="sxs-lookup"><span data-stu-id="44559-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="44559-110">Per ulteriori note sull'utilizzo, vedere la pagina [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .</span><span class="sxs-lookup"><span data-stu-id="44559-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="44559-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44559-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="44559-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="44559-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44559-113">*ch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44559-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44559-114">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="44559-114">Type: **WCHAR**</span></span>

<span data-ttu-id="44559-115">Carattere Unicode da verificare.</span><span class="sxs-lookup"><span data-stu-id="44559-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44559-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44559-116">Return value</span></span>

<span data-ttu-id="44559-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="44559-117">Type: **BOOL**</span></span>

<span data-ttu-id="44559-118">Se il carattere è alfanumerico, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="44559-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="44559-119">Se il carattere non è alfanumerico, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="44559-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="44559-120">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="44559-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="44559-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="44559-121">Remarks</span></span>

<span data-ttu-id="44559-122">**IsCharAlphaNumericWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="44559-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="44559-123">Il metodo preferito consiste nell'usare [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="44559-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="44559-124">**IsCharAlphaNumericWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 28.</span><span class="sxs-lookup"><span data-stu-id="44559-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="44559-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44559-125">Requirements</span></span>



| <span data-ttu-id="44559-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="44559-126">Requirement</span></span> | <span data-ttu-id="44559-127">Valore</span><span class="sxs-lookup"><span data-stu-id="44559-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44559-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44559-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44559-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="44559-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44559-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44559-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44559-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44559-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44559-132">DLL</span><span class="sxs-lookup"><span data-stu-id="44559-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44559-133"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="44559-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44559-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44559-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44559-135">**IsCharAlphaNumeric**</span><span class="sxs-lookup"><span data-stu-id="44559-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
