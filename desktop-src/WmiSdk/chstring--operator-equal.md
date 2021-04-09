---
description: L'operatore di assegnazione CHString (=) reinizializza un oggetto CHString esistente con nuovi dati.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString:: operator = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050124"
---
# <a name="chstringoperator"></a><span data-ttu-id="b8070-103">CHString:: operator =</span><span class="sxs-lookup"><span data-stu-id="b8070-103">CHString::operator=</span></span>

<span data-ttu-id="b8070-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="b8070-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b8070-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="b8070-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b8070-106">L'operatore di assegnazione [**CHString**](chstring.md) (=) reinizializza un oggetto CHString esistente con nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="b8070-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="b8070-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8070-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8070-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span><span class="sxs-lookup"><span data-stu-id="b8070-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="b8070-109">Assegna una stringa [**CHString**](chstring.md) a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8070-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="b8070-110"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="b8070-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="b8070-111">Assegna un carattere a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8070-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="b8070-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*</span><span class="sxs-lookup"><span data-stu-id="b8070-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="b8070-113">Assegna una stringa con terminazione **null** a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b8070-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8070-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8070-114">Remarks</span></span>

<span data-ttu-id="b8070-115">Se la stringa di destinazione, ovvero il lato sinistro, è già abbastanza grande da archiviare i nuovi dati, non viene eseguita alcuna nuova allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="b8070-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="b8070-116">Tuttavia, le eccezioni di memoria possono verificarsi quando si usa l'operatore di assegnazione perché la nuova risorsa di archiviazione viene spesso allocata per conservare l'oggetto [**CHString**](chstring.md) risultante.</span><span class="sxs-lookup"><span data-stu-id="b8070-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b8070-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8070-117">Examples</span></span>

<span data-ttu-id="b8070-118">Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo di **CHString:: operator =**:</span><span class="sxs-lookup"><span data-stu-id="b8070-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="b8070-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8070-119">Requirements</span></span>



| <span data-ttu-id="b8070-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8070-120">Requirement</span></span> | <span data-ttu-id="b8070-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8070-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8070-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8070-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8070-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8070-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b8070-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8070-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8070-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8070-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b8070-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8070-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8070-127"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8070-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b8070-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8070-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8070-129"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8070-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="b8070-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b8070-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8070-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8070-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8070-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8070-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8070-133">**CHString**</span><span class="sxs-lookup"><span data-stu-id="b8070-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

