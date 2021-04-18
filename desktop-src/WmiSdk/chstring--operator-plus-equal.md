---
description: L'operatore di concatenazione + = unisce i caratteri alla fine di questa stringa. L'operatore accetta un altro oggetto CHString, un puntatore a caratteri o un singolo carattere.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313200"
---
# <a name="chstringoperator"></a><span data-ttu-id="cc03c-104">CHString:: operator + =</span><span class="sxs-lookup"><span data-stu-id="cc03c-104">CHString::operator+=</span></span>

<span data-ttu-id="cc03c-105">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="cc03c-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="cc03c-106">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="cc03c-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="cc03c-107">L'operatore di concatenazione + = unisce i caratteri alla fine di questa stringa.</span><span class="sxs-lookup"><span data-stu-id="cc03c-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="cc03c-108">L'operatore accetta un altro oggetto [**CHString**](chstring.md) , un puntatore a caratteri o un singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="cc03c-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="cc03c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc03c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc03c-110"><span id="string"></span><span id="STRING"></span>*stringa*</span><span class="sxs-lookup"><span data-stu-id="cc03c-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="cc03c-111">Stringa [**CHString**](chstring.md) che concatena a questa stringa.</span><span class="sxs-lookup"><span data-stu-id="cc03c-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="cc03c-112"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="cc03c-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="cc03c-113">Carattere da concatenare a questa stringa.</span><span class="sxs-lookup"><span data-stu-id="cc03c-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="cc03c-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="cc03c-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="cc03c-115">Puntatore a una stringa con terminazione **null** da concatenare a questa stringa.</span><span class="sxs-lookup"><span data-stu-id="cc03c-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc03c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc03c-116">Remarks</span></span>

<span data-ttu-id="cc03c-117">Tenere presente che le eccezioni di memoria possono verificarsi quando si usa questo operatore di concatenazione perché è possibile allocare una nuova risorsa di archiviazione per i caratteri aggiunti a questo oggetto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="cc03c-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="cc03c-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="cc03c-118">Examples</span></span>

<span data-ttu-id="cc03c-119">Nell'esempio seguente viene illustrato l'utilizzo di **CHString:: operator + =**:</span><span class="sxs-lookup"><span data-stu-id="cc03c-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="cc03c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc03c-120">Requirements</span></span>



| <span data-ttu-id="cc03c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc03c-121">Requirement</span></span> | <span data-ttu-id="cc03c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cc03c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc03c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc03c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cc03c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc03c-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="cc03c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc03c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cc03c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc03c-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="cc03c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc03c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc03c-128"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc03c-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc03c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc03c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc03c-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc03c-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="cc03c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cc03c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc03c-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc03c-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc03c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc03c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc03c-134">**CHString**</span><span class="sxs-lookup"><span data-stu-id="cc03c-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

