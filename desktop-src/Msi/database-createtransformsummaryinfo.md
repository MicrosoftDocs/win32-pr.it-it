---
description: Il metodo CreateTransformSummaryInfo dell'oggetto di database crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente. Questo metodo compila le proprietà con la base e il riferimento ProductCode e ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Metodo database. CreateTransformSummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326547"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="5e4e6-104">Metodo database. CreateTransformSummaryInfo</span><span class="sxs-lookup"><span data-stu-id="5e4e6-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="5e4e6-105">Il metodo **CreateTransformSummaryInfo** dell'oggetto di [**database**](database-object.md) crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="5e4e6-106">Questo metodo compila le proprietà con la base e il riferimento [**ProductCode**](productcode.md) e [**ProductVersion**](productversion.md).</span><span class="sxs-lookup"><span data-stu-id="5e4e6-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4e6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e4e6-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="5e4e6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e4e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4e6-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="5e4e6-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4e6-110">Database obbligatorio che non include le modifiche.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="5e4e6-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="5e4e6-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4e6-112">Nome del file di trasformazione generato.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-112">The name of the generated transform file.</span></span> <span data-ttu-id="5e4e6-113">Questo indirizzo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5e4e6-114">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="5e4e6-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4e6-115">Condizioni di errore obbligatorie che devono essere evitate quando si applica la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="5e4e6-116">Combinare uno o più dei seguenti valori di condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="5e4e6-117">Nome della condizione di errore</span><span class="sxs-lookup"><span data-stu-id="5e4e6-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="5e4e6-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5e4e6-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="5e4e6-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="5e4e6-120">Nessuna delle condizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="5e4e6-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="5e4e6-122">Aggiunge una riga già esistente.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="5e4e6-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="5e4e6-124">Elimina una riga inesistente.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="5e4e6-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="5e4e6-126">Aggiunge una tabella già esistente.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="5e4e6-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="5e4e6-128">Elimina una tabella che non esiste.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="5e4e6-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="5e4e6-130">Aggiorna una riga che non esiste.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="5e4e6-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="5e4e6-132">Le tabelle codici di trasformazione e database non corrispondono e nessuna tabella codici è neutra.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e4e6-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="5e4e6-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="5e4e6-134">Obbligatorio quando la trasformazione viene applicata a un database; Mostra le proprietà da convalidare per verificare che questa trasformazione possa essere applicata al database.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="5e4e6-135">Tutte le proprietà sono contenute nel [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="5e4e6-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="5e4e6-136">Combinare uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="5e4e6-137">Flag di convalida</span><span class="sxs-lookup"><span data-stu-id="5e4e6-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="5e4e6-138">Significato</span><span class="sxs-lookup"><span data-stu-id="5e4e6-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="5e4e6-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="5e4e6-140">Nessuna convalida eseguita.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="5e4e6-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="5e4e6-142">La lingua predefinita deve corrispondere al database di base.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="5e4e6-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="5e4e6-144">Il prodotto deve corrispondere al database di base.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="5e4e6-145">Per convalidare la versione del prodotto, è necessario innanzitutto scegliere uno o più di questi tre flag per indicare la quantità di versione da verificare.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="5e4e6-146">Flag di convalida</span><span class="sxs-lookup"><span data-stu-id="5e4e6-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="5e4e6-147">Significato</span><span class="sxs-lookup"><span data-stu-id="5e4e6-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="5e4e6-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="5e4e6-149">Verifica solo la versione principale.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="5e4e6-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="5e4e6-151">Verifica solo la versione principale e secondaria.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="5e4e6-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="5e4e6-153">Controlla le versioni principale, secondaria e di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="5e4e6-154">Quindi scegliere una delle opzioni seguenti per indicare la relazione necessaria tra la versione del prodotto del database a cui viene applicata la trasformazione e quella del database di base.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="5e4e6-155">Flag di convalida</span><span class="sxs-lookup"><span data-stu-id="5e4e6-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="5e4e6-156">Significato</span><span class="sxs-lookup"><span data-stu-id="5e4e6-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="5e4e6-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="5e4e6-158">Versione < versione di base applicata</span><span class="sxs-lookup"><span data-stu-id="5e4e6-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="5e4e6-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="5e4e6-160">Versione <applicata = versione di base</span><span class="sxs-lookup"><span data-stu-id="5e4e6-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="5e4e6-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="5e4e6-162">Versione applicata = versione di base</span><span class="sxs-lookup"><span data-stu-id="5e4e6-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="5e4e6-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="5e4e6-164">Versione >applicata = versione di base</span><span class="sxs-lookup"><span data-stu-id="5e4e6-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="5e4e6-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="5e4e6-166">Versione > versione di base applicata</span><span class="sxs-lookup"><span data-stu-id="5e4e6-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="5e4e6-167">Per verificare che la trasformazione venga applicata a un pacchetto con il [**UpgradeCode**](upgradecode.md)appropriato, impostare il flag seguente.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="5e4e6-168">Flag di convalida</span><span class="sxs-lookup"><span data-stu-id="5e4e6-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="5e4e6-169">Significato</span><span class="sxs-lookup"><span data-stu-id="5e4e6-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="5e4e6-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="5e4e6-171">Verifica che la trasformazione sia il [**UpgradeCode**](upgradecode.md)appropriato.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4e6-172">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e4e6-172">Return value</span></span>

<span data-ttu-id="5e4e6-173">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e4e6-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e4e6-174">Remarks</span></span>

<span data-ttu-id="5e4e6-175">Per creare un flusso di informazioni di riepilogo per una trasformazione, è necessario definire le proprietà [**ProductCode**](productcode.md) e [**ProductVersion**](productversion.md) nelle tabelle delle [proprietà](property-table.md) dei database di base e di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="5e4e6-176">Se si usa msiTransformValidationUpgradeCode, è necessario definire la proprietà [**UpgradeCode**](upgradecode.md) in entrambi i database.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4e6-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e4e6-177">Requirements</span></span>



| <span data-ttu-id="5e4e6-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e4e6-178">Requirement</span></span> | <span data-ttu-id="5e4e6-179">Valore</span><span class="sxs-lookup"><span data-stu-id="5e4e6-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4e6-180">Versione</span><span class="sxs-lookup"><span data-stu-id="5e4e6-180">Version</span></span><br/> | <span data-ttu-id="5e4e6-181">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5e4e6-182">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e4e6-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5e4e6-183">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e4e6-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5e4e6-184">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4e6-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e4e6-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4e6-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5e4e6-186">IID</span><span class="sxs-lookup"><span data-stu-id="5e4e6-186">IID</span></span><br/>     | <span data-ttu-id="5e4e6-187">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5e4e6-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5e4e6-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e4e6-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4e6-189">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="5e4e6-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




