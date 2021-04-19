---
description: Il metodo OpenView dell'oggetto di database restituisce un oggetto visualizzazione che rappresenta la query specificata da una stringa SQL.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Metodo database. OpenView (certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333057"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="075a9-103">Metodo database. OpenView</span><span class="sxs-lookup"><span data-stu-id="075a9-103">Database.OpenView method</span></span>

<span data-ttu-id="075a9-104">Il metodo **OpenView** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**visualizzazione**](view-object.md) che rappresenta la query specificata da una stringa SQL.</span><span class="sxs-lookup"><span data-stu-id="075a9-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="075a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="075a9-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="075a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="075a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075a9-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="075a9-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="075a9-108">Stringa di query SQL richiesta.</span><span class="sxs-lookup"><span data-stu-id="075a9-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075a9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="075a9-109">Return value</span></span>

<span data-ttu-id="075a9-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="075a9-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="075a9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="075a9-111">Remarks</span></span>

<span data-ttu-id="075a9-112">Per informazioni sulla sintassi SQL implementata nel programma di installazione, vedere [sintassi SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="075a9-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="075a9-113">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="075a9-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="075a9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="075a9-114">Requirements</span></span>



| <span data-ttu-id="075a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="075a9-115">Requirement</span></span> | <span data-ttu-id="075a9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="075a9-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075a9-117">Versione</span><span class="sxs-lookup"><span data-stu-id="075a9-117">Version</span></span><br/> | <span data-ttu-id="075a9-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="075a9-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="075a9-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="075a9-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="075a9-120">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="075a9-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="075a9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="075a9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="075a9-122"><dt>Certview. h</dt></span><span class="sxs-lookup"><span data-stu-id="075a9-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="075a9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="075a9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="075a9-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="075a9-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="075a9-125">IID</span><span class="sxs-lookup"><span data-stu-id="075a9-125">IID</span></span><br/>     | <span data-ttu-id="075a9-126">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="075a9-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="075a9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="075a9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075a9-128">**Database**</span><span class="sxs-lookup"><span data-stu-id="075a9-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="075a9-129">Sintassi SQL</span><span class="sxs-lookup"><span data-stu-id="075a9-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




