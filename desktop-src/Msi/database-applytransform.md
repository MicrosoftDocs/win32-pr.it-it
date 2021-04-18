---
description: Il metodo ApplyTransform dell'oggetto di database applica la trasformazione al database.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Metodo database. ApplyTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331616"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="834f6-103">Metodo database. ApplyTransform</span><span class="sxs-lookup"><span data-stu-id="834f6-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="834f6-104">Il metodo **ApplyTransform** dell'oggetto di [**database**](database-object.md) applica la trasformazione al database.</span><span class="sxs-lookup"><span data-stu-id="834f6-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="834f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="834f6-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="834f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="834f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834f6-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="834f6-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="834f6-108">Percorso del file di trasformazione da applicare.</span><span class="sxs-lookup"><span data-stu-id="834f6-108">Path to the transform file being applied.</span></span> <span data-ttu-id="834f6-109">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="834f6-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="834f6-110">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="834f6-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="834f6-111">Specifica le condizioni di errore che devono essere evitate.</span><span class="sxs-lookup"><span data-stu-id="834f6-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="834f6-112">Specificare come una combinazione dei valori interi seguenti.</span><span class="sxs-lookup"><span data-stu-id="834f6-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="834f6-113">Condizione di errore</span><span class="sxs-lookup"><span data-stu-id="834f6-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="834f6-114">Significato</span><span class="sxs-lookup"><span data-stu-id="834f6-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="834f6-115"><dt></dt> <dt>0x0001</dt> msiTransformErrorAddExistingRow</span><span class="sxs-lookup"><span data-stu-id="834f6-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="834f6-116">Aggiunge una riga già esistente.</span><span class="sxs-lookup"><span data-stu-id="834f6-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="834f6-117"><dt></dt> <dt>0x0002</dt> msiTransformErrorDeleteNonExistingRow</span><span class="sxs-lookup"><span data-stu-id="834f6-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="834f6-118">Elimina una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="834f6-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="834f6-119"><dt></dt> <dt>0x0004</dt> msiTransformErrorAddExistingTable</span><span class="sxs-lookup"><span data-stu-id="834f6-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="834f6-120">Aggiunge una tabella già esistente.</span><span class="sxs-lookup"><span data-stu-id="834f6-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="834f6-121"><dt></dt> <dt>0x0008</dt> msiTransformErrorDeleteNonExistingTable</span><span class="sxs-lookup"><span data-stu-id="834f6-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="834f6-122">Elimina una tabella che non esiste.</span><span class="sxs-lookup"><span data-stu-id="834f6-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="834f6-123"><dt></dt> <dt>0x0010</dt> msiTransformErrorUpdateNonExistingRow</span><span class="sxs-lookup"><span data-stu-id="834f6-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="834f6-124">Aggiorna una riga che non esiste.</span><span class="sxs-lookup"><span data-stu-id="834f6-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="834f6-125"><dt></dt> <dt>0x0020</dt> msiTransformErrorChangeCodePage</span><span class="sxs-lookup"><span data-stu-id="834f6-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="834f6-126">Le tabelle codici di trasformazione e database non corrispondono e nessuna tabella codici è neutra.</span><span class="sxs-lookup"><span data-stu-id="834f6-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="834f6-127"><dt></dt> <dt>0x0100</dt> msiTransformErrorViewTransform</span><span class="sxs-lookup"><span data-stu-id="834f6-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="834f6-128">Crea la [ \_ tabella transformview](-transformview-table.md)temporanea.</span><span class="sxs-lookup"><span data-stu-id="834f6-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834f6-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="834f6-129">Return value</span></span>

<span data-ttu-id="834f6-130">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="834f6-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="834f6-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="834f6-131">Remarks</span></span>

<span data-ttu-id="834f6-132">Il metodo **ApplyTransform** ritarda la trasformazione delle tabelle fino all'ultimo momento possibile.</span><span class="sxs-lookup"><span data-stu-id="834f6-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="834f6-133">I passaggi eseguiti in **ApplyTransform** sono la trasformazione immediata dei cataloghi di tabelle e colonne per il database.</span><span class="sxs-lookup"><span data-stu-id="834f6-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="834f6-134">I cataloghi della tabella e della colonna vengono aggiornati in base alla tabella aggiunta o eliminata e alla colonna aggiunta (non è consentita l'eliminazione di colonne).</span><span class="sxs-lookup"><span data-stu-id="834f6-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="834f6-135">Se una tabella è attualmente caricata in memoria e deve essere trasformata, viene trasformata.</span><span class="sxs-lookup"><span data-stu-id="834f6-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="834f6-136">In caso contrario, lo stato della tabella viene impostato su che richiede una trasformazione in modo che quando viene caricata la tabella o quando viene eseguito il commit del database, viene applicata la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="834f6-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="834f6-137">La trasformazione in questa istanza indica che i dati effettivi (riga) della tabella vengono aggiunti, eliminati o aggiornati.</span><span class="sxs-lookup"><span data-stu-id="834f6-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="834f6-138">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="834f6-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="834f6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="834f6-139">Requirements</span></span>



| <span data-ttu-id="834f6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="834f6-140">Requirement</span></span> | <span data-ttu-id="834f6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="834f6-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="834f6-142">Versione</span><span class="sxs-lookup"><span data-stu-id="834f6-142">Version</span></span><br/> | <span data-ttu-id="834f6-143">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="834f6-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="834f6-144">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="834f6-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="834f6-145">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="834f6-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="834f6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="834f6-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="834f6-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834f6-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="834f6-148">IID</span><span class="sxs-lookup"><span data-stu-id="834f6-148">IID</span></span><br/>     | <span data-ttu-id="834f6-149">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="834f6-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="834f6-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="834f6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834f6-151">**Database**</span><span class="sxs-lookup"><span data-stu-id="834f6-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="834f6-152">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="834f6-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




