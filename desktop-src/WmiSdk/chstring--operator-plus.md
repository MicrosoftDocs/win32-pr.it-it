---
description: L'operatore di concatenazione + unisce due stringhe e restituisce un oggetto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758219"
---
# <a name="chstringoperator"></a><span data-ttu-id="60200-103">CHString:: operator +</span><span class="sxs-lookup"><span data-stu-id="60200-103">CHString::operator+</span></span>

<span data-ttu-id="60200-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="60200-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="60200-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="60200-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="60200-106">L'operatore di concatenazione + unisce due stringhe e restituisce un oggetto [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="60200-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="60200-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="60200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60200-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*</span><span class="sxs-lookup"><span data-stu-id="60200-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="60200-109">[**CHString**](chstring.md) stringhe concatenate.</span><span class="sxs-lookup"><span data-stu-id="60200-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="60200-110"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="60200-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="60200-111">Carattere che concatena a una stringa o una stringa concatenata a un carattere.</span><span class="sxs-lookup"><span data-stu-id="60200-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="60200-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="60200-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="60200-113">Puntatore a una stringa di caratteri con terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="60200-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="60200-114">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="60200-114">Return Values</span></span>

<span data-ttu-id="60200-115">Questo operatore di concatenazione restituisce un oggetto [**CHString**](chstring.md) che rappresenta il risultato temporaneo della concatenazione.</span><span class="sxs-lookup"><span data-stu-id="60200-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="60200-116">Questo valore restituito rende possibile combinare più concatenazioni nella stessa espressione.</span><span class="sxs-lookup"><span data-stu-id="60200-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="60200-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="60200-117">Remarks</span></span>

<span data-ttu-id="60200-118">Una delle due stringhe di argomento deve essere un oggetto [**CHString**](chstring.md) . l'altro può essere un puntatore a caratteri o un carattere.</span><span class="sxs-lookup"><span data-stu-id="60200-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="60200-119">Tenere presente che le eccezioni di memoria possono verificarsi quando si usa l'operatore di concatenazione perché è possibile allocare una nuova risorsa di archiviazione per contenere dati temporanei.</span><span class="sxs-lookup"><span data-stu-id="60200-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="60200-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="60200-120">Examples</span></span>

<span data-ttu-id="60200-121">L'esempio di codice seguente illustra l'uso di **CHString:: operator +**:</span><span class="sxs-lookup"><span data-stu-id="60200-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="60200-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60200-122">Requirements</span></span>



| <span data-ttu-id="60200-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60200-123">Requirement</span></span> | <span data-ttu-id="60200-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60200-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60200-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60200-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60200-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60200-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="60200-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60200-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60200-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60200-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="60200-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60200-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="60200-130"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60200-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="60200-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="60200-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="60200-132"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60200-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="60200-133">DLL</span><span class="sxs-lookup"><span data-stu-id="60200-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60200-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60200-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60200-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60200-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60200-136">**CHString**</span><span class="sxs-lookup"><span data-stu-id="60200-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

