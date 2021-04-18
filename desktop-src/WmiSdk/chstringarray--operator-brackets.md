---
description: Questi operatori di pedice impostano o ottengono l'elemento in corrispondenza dell'indice specificato. Questi operatori rappresentano un comodo sostituto per i metodi SetAt e GetA.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray:: operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316992"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="0d45c-104">Operatore \[ CHStringArray:: \]</span><span class="sxs-lookup"><span data-stu-id="0d45c-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="0d45c-105">\[La classe [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="0d45c-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0d45c-106">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="0d45c-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0d45c-107">Questi operatori di pedice impostano o ottengono l'elemento in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="0d45c-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="0d45c-108">Questi operatori rappresentano un comodo sostituto per i metodi [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) e [**Geta**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .</span><span class="sxs-lookup"><span data-stu-id="0d45c-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="0d45c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d45c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d45c-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="0d45c-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="0d45c-111">Indice integer maggiore o uguale a zero e minore o uguale al valore restituito da [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="0d45c-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="0d45c-112">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="0d45c-112">Return Values</span></span>

<span data-ttu-id="0d45c-113">Gli operatori di pedice restituiscono l'elemento puntatore [**CHString**](chstring.md) attualmente in corrispondenza di questo indice.</span><span class="sxs-lookup"><span data-stu-id="0d45c-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d45c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d45c-114">Remarks</span></span>

<span data-ttu-id="0d45c-115">È possibile usare il primo operatore, che chiama per le matrici che non sono **const**, a destra (r-value) o il lato sinistro (l-value) di un'istruzione di assegnazione.</span><span class="sxs-lookup"><span data-stu-id="0d45c-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="0d45c-116">Il secondo, che chiama per le matrici **const** , può essere utilizzato solo a destra.</span><span class="sxs-lookup"><span data-stu-id="0d45c-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="0d45c-117">La versione di debug della libreria dichiara se l'indice (sul lato sinistro o destro di un'istruzione di assegnazione) non è più limitato.</span><span class="sxs-lookup"><span data-stu-id="0d45c-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="0d45c-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="0d45c-118">Examples</span></span>

<span data-ttu-id="0d45c-119">Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo di [**CHStringArray:: operator \[ \]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d45c-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="0d45c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d45c-120">Requirements</span></span>



| <span data-ttu-id="0d45c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d45c-121">Requirement</span></span> | <span data-ttu-id="0d45c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0d45c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d45c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d45c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d45c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d45c-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0d45c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d45c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d45c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d45c-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0d45c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d45c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d45c-128"><dt>ChStrArr. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d45c-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0d45c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d45c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d45c-130"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d45c-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="0d45c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0d45c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d45c-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d45c-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d45c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d45c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d45c-134">**CHStringArray:: Add**</span><span class="sxs-lookup"><span data-stu-id="0d45c-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="0d45c-135">[**CHStringArray:: GetA**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="0d45c-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="0d45c-136">[**CHStringArray:: SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="0d45c-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

