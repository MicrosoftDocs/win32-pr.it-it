---
description: Il metodo Execute dell'oggetto View usa il token Question Mark per rappresentare i parametri in un'istruzione SQL. Per altre informazioni, vedere Sintassi SQL. I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemetodo carino
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324769"
---
# <a name="viewexecute-method"></a><span data-ttu-id="21412-105">View.Exemetodo carino</span><span class="sxs-lookup"><span data-stu-id="21412-105">View.Execute method</span></span>

<span data-ttu-id="21412-106">Il metodo **Execute** dell'oggetto [**View**](view-object.md) usa il token Question Mark per rappresentare i parametri in un'istruzione SQL.</span><span class="sxs-lookup"><span data-stu-id="21412-106">The **Execute** method of the [**View**](view-object.md) object uses the question mark token to represent parameters in an SQL statement.</span></span> <span data-ttu-id="21412-107">Per altre informazioni, vedere [sintassi SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="21412-107">For more information, see [SQL Syntax](sql-syntax.md).</span></span> <span data-ttu-id="21412-108">I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.</span><span class="sxs-lookup"><span data-stu-id="21412-108">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span>

## <a name="syntax"></a><span data-ttu-id="21412-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21412-109">Syntax</span></span>


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="21412-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="21412-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21412-111">*record*</span><span class="sxs-lookup"><span data-stu-id="21412-111">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="21412-112">Oggetti [**record**](record-object.md) facoltativi che contengono i valori che sostituiscono i token di parametro (?) nella query SQL.</span><span class="sxs-lookup"><span data-stu-id="21412-112">Optional [**Record**](record-object.md) objects that contains the values that replace the parameter tokens (?) in the SQL query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21412-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21412-113">Return value</span></span>

<span data-ttu-id="21412-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="21412-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21412-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="21412-115">Remarks</span></span>

<span data-ttu-id="21412-116">Questo metodo deve essere chiamato prima di qualsiasi chiamata al metodo [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="21412-116">This method must be called before any calls to the [**Fetch**](view-fetch.md) method.</span></span>

<span data-ttu-id="21412-117">Se la query SQL specifica valori con marcatori di parametro (?), è necessario specificare un record contenente tutti i valori di sostituzione, che devono essere nello stesso ordine e dello stesso tipo di dati dei marcatori di parametro.</span><span class="sxs-lookup"><span data-stu-id="21412-117">If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values, which must be in the same order and of the same data type as the parameter markers.</span></span> <span data-ttu-id="21412-118">Quando questo metodo viene utilizzato con le query di inserimento e aggiornamento, i token dei punti interrogativi devono precedere tutti i valori senza parametri.</span><span class="sxs-lookup"><span data-stu-id="21412-118">When this method is used with INSERT and UPDATE queries, the question mark tokens must precede all the non-parameterized values.</span></span>

<span data-ttu-id="21412-119">Ad esempio, queste query sono valide:</span><span class="sxs-lookup"><span data-stu-id="21412-119">For example, these queries are valid:</span></span>

<span data-ttu-id="21412-120">AGGIORNAMENTO {Table-list} SET {Column} =?</span><span class="sxs-lookup"><span data-stu-id="21412-120">UPDATE {table-list} SET {column}= ?</span></span> <span data-ttu-id="21412-121">, {Column} = {Constant}</span><span class="sxs-lookup"><span data-stu-id="21412-121">, {column}= {constant}</span></span>

<span data-ttu-id="21412-122">INSERT INTO {TABLE} ({Column-List}) valori (?, {Constant-List})</span><span class="sxs-lookup"><span data-stu-id="21412-122">INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})</span></span>

<span data-ttu-id="21412-123">Tuttavia, queste query non sono valide:</span><span class="sxs-lookup"><span data-stu-id="21412-123">However these queries are invalid:</span></span>

<span data-ttu-id="21412-124">AGGIORNAMENTO {Table-list} SET {Column} = {Constant}, {Column} =?</span><span class="sxs-lookup"><span data-stu-id="21412-124">UPDATE {table-list} SET {column}= {constant}, {column}=?</span></span>

<span data-ttu-id="21412-125">INSERIRE i valori {Table} ({Column-List}) ({Constant-list},?</span><span class="sxs-lookup"><span data-stu-id="21412-125">INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ?</span></span> <span data-ttu-id="21412-126">)</span><span class="sxs-lookup"><span data-stu-id="21412-126">)</span></span>

<span data-ttu-id="21412-127">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="21412-127">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="21412-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21412-128">Requirements</span></span>



| <span data-ttu-id="21412-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="21412-129">Requirement</span></span> | <span data-ttu-id="21412-130">Valore</span><span class="sxs-lookup"><span data-stu-id="21412-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21412-131">Versione</span><span class="sxs-lookup"><span data-stu-id="21412-131">Version</span></span><br/> | <span data-ttu-id="21412-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21412-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="21412-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21412-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="21412-134">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="21412-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="21412-135">DLL</span><span class="sxs-lookup"><span data-stu-id="21412-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="21412-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21412-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="21412-137">IID</span><span class="sxs-lookup"><span data-stu-id="21412-137">IID</span></span><br/>     | <span data-ttu-id="21412-138">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="21412-138">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




