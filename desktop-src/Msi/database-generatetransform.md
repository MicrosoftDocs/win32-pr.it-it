---
description: Il metodo GenerateTransform dell'oggetto di database crea una trasformazione che, quando applicata al database dell'oggetto, restituisce il database di riferimento. La trasformazione viene archiviata nell'oggetto di archiviazione.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Metodo database. GenerateTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326899"
---
# <a name="databasegeneratetransform-method"></a><span data-ttu-id="a144e-104">Metodo database. GenerateTransform</span><span class="sxs-lookup"><span data-stu-id="a144e-104">Database.GenerateTransform method</span></span>

<span data-ttu-id="a144e-105">Il metodo **GenerateTransform** dell'oggetto di [**database**](database-object.md) crea una [*trasformazione*](t-gly.md) che, quando applicata al database dell'oggetto, restituisce il database di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a144e-105">The **GenerateTransform** method of the [**Database**](database-object.md) object creates a [*transform*](t-gly.md) that, when applied to the object database, results in the reference database.</span></span> <span data-ttu-id="a144e-106">La trasformazione viene archiviata nell'oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a144e-106">The transform is stored in the storage object.</span></span>

<span data-ttu-id="a144e-107">Se la trasformazione deve essere applicata durante un'installazione, è necessario usare il metodo [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) per popolare il flusso di informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="a144e-107">If the transform is to be applied during an installation you must use the [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) method to populate the summary information stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="a144e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a144e-108">Syntax</span></span>


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a><span data-ttu-id="a144e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a144e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a144e-110">*reference*</span><span class="sxs-lookup"><span data-stu-id="a144e-110">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="a144e-111">Database obbligatorio che non include le modifiche.</span><span class="sxs-lookup"><span data-stu-id="a144e-111">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="a144e-112">*storage*</span><span class="sxs-lookup"><span data-stu-id="a144e-112">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="a144e-113">Nome del file di trasformazione generato.</span><span class="sxs-lookup"><span data-stu-id="a144e-113">The name of the generated transform file.</span></span> <span data-ttu-id="a144e-114">Questo indirizzo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a144e-114">This is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a144e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a144e-115">Return value</span></span>

<span data-ttu-id="a144e-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a144e-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a144e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a144e-117">Remarks</span></span>

<span data-ttu-id="a144e-118">Una trasformazione può aggiungere colonne chiave non primarie alla fine di una tabella.</span><span class="sxs-lookup"><span data-stu-id="a144e-118">A transform can add non-primary key columns to the end of a table.</span></span> <span data-ttu-id="a144e-119">Non è possibile creare una trasformazione che aggiunge colonne chiave primaria a una tabella.</span><span class="sxs-lookup"><span data-stu-id="a144e-119">A transform cannot be created that adds primary key columns to a table.</span></span> <span data-ttu-id="a144e-120">Non è possibile creare una trasformazione che modifichi l'ordine, i nomi o le definizioni delle colonne.</span><span class="sxs-lookup"><span data-stu-id="a144e-120">A transform cannot be created that changes the order, names, or definitions of columns.</span></span>

<span data-ttu-id="a144e-121">Questo metodo restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="a144e-121">This method returns a Boolean value.</span></span> <span data-ttu-id="a144e-122">Restituisce TRUE se viene generata una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="a144e-122">It returns TRUE if a transform is generated.</span></span> <span data-ttu-id="a144e-123">Restituisce FALSE se non viene generata alcuna trasformazione perché non vi sono differenze tra i due database.</span><span class="sxs-lookup"><span data-stu-id="a144e-123">It returns FALSE if a transform is not generated because there are no differences between the two databases.</span></span> <span data-ttu-id="a144e-124">Se il metodo ha esito negativo, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="a144e-124">If the method fails, it generates an error.</span></span>

<span data-ttu-id="a144e-125">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="a144e-125">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a144e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a144e-126">Requirements</span></span>



| <span data-ttu-id="a144e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a144e-127">Requirement</span></span> | <span data-ttu-id="a144e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a144e-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a144e-129">Versione</span><span class="sxs-lookup"><span data-stu-id="a144e-129">Version</span></span><br/> | <span data-ttu-id="a144e-130">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a144e-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a144e-131">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a144e-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a144e-132">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a144e-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a144e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a144e-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="a144e-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a144e-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a144e-135">IID</span><span class="sxs-lookup"><span data-stu-id="a144e-135">IID</span></span><br/>     | <span data-ttu-id="a144e-136">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a144e-136">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a144e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a144e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a144e-138">**Database**</span><span class="sxs-lookup"><span data-stu-id="a144e-138">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="a144e-139">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="a144e-139">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




