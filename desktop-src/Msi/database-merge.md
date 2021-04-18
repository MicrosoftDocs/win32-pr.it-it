---
description: Il metodo Merge dell'oggetto di database unisce il database di riferimento al database di base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Metodo database. merge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329752"
---
# <a name="databasemerge-method"></a><span data-ttu-id="7310f-103">Metodo database. merge</span><span class="sxs-lookup"><span data-stu-id="7310f-103">Database.Merge method</span></span>

<span data-ttu-id="7310f-104">Il metodo **merge** dell'oggetto di [**database**](database-object.md) unisce il database di riferimento al database di base.</span><span class="sxs-lookup"><span data-stu-id="7310f-104">The **Merge** method of the [**Database**](database-object.md) object merges the reference database with the base database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7310f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7310f-105">Syntax</span></span>


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a><span data-ttu-id="7310f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7310f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7310f-107">*reference*</span><span class="sxs-lookup"><span data-stu-id="7310f-107">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="7310f-108">Oggetto di [**database**](database-object.md) obbligatorio da unire nel database.</span><span class="sxs-lookup"><span data-stu-id="7310f-108">The required [**Database**](database-object.md) object to be merged into the database.</span></span>

</dd> <dt>

<span data-ttu-id="7310f-109">*errorTable*</span><span class="sxs-lookup"><span data-stu-id="7310f-109">*errorTable*</span></span> 
</dt> <dd>

<span data-ttu-id="7310f-110">Nome facoltativo di una tabella che contiene i nomi delle tabelle contenenti conflitti di merge, il numero di righe in conflitto all'interno della tabella e un riferimento alla tabella con il conflitto di Unione.</span><span class="sxs-lookup"><span data-stu-id="7310f-110">An optional name of a table to contain the names of the tables containing merge conflicts, the number of conflicting rows within the table, and a reference to the table with the merge conflict.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7310f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7310f-111">Return value</span></span>

<span data-ttu-id="7310f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7310f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7310f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7310f-113">Remarks</span></span>

<span data-ttu-id="7310f-114">Non è possibile usare la funzione [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e il metodo **merge** dell'oggetto di [**database**](database-object.md) per unire un modulo incluso in un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="7310f-114">The [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function and the **Merge** method of the [**Database**](database-object.md) object cannot be used to merge a module included within an installation package.</span></span> <span data-ttu-id="7310f-115">Non devono essere utilizzate per unire i [moduli unione](merge-modules.md) in un pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7310f-115">They should not be used to merge [Merge Modules](merge-modules.md) into a Windows Installer package.</span></span> <span data-ttu-id="7310f-116">Per includere un modulo merge in un pacchetto di installazione, è necessario che gli autori dei pacchetti di installazione seguano le linee guida descritte nell'argomento [Applying merge modules](applying-merge-modules.md) .</span><span class="sxs-lookup"><span data-stu-id="7310f-116">To include a merge module in an installation package, authors of installation packages should follow the guidelines that are described in the [Applying Merge Modules](applying-merge-modules.md) topic.</span></span>

<span data-ttu-id="7310f-117">Il metodo **merge** non esegue la copia su [file CAB](cabinet-files.md) incorporati o [trasformazioni incorporate](embedded-transforms.md) dal database di riferimento nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7310f-117">The **Merge** method does not copy over embedded [cabinet files](cabinet-files.md) or [embedded transforms](embedded-transforms.md) from the reference database into the target database.</span></span> <span data-ttu-id="7310f-118">I flussi di dati incorporati elencati nella tabella [binaria](binary-table.md) o nella [tabella delle icone](icon-table.md) vengono copiati dal database di riferimento al database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7310f-118">Embedded data streams that are listed in the [Binary Table](binary-table.md) or [Icon Table](icon-table.md) are copied from the reference database to the target database.</span></span> <span data-ttu-id="7310f-119">Le archiviazioni incorporate nel database di riferimento non vengono copiate nel database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7310f-119">Storages embedded in the reference database are not copied to the target database.</span></span>

<span data-ttu-id="7310f-120">Se non viene fornita alcuna tabella, il messaggio di errore generale fornisce il numero di tabelle contenenti conflitti di merge.</span><span class="sxs-lookup"><span data-stu-id="7310f-120">If no table is provided, the general error message provides the number of tables containing merge conflicts.</span></span> <span data-ttu-id="7310f-121">È possibile passare qualsiasi tabella, ma tutte le altre colonne devono ammettere i valori null perché l'operazione di aggiornamento della [tabella degli errori](error-table.md) ha esito negativo se una colonna non ammette i valori null.</span><span class="sxs-lookup"><span data-stu-id="7310f-121">Any table can be passed in, but all other columns must be nullable because the operation to update the [Error Table](error-table.md) fails if a column is not nullable.</span></span> <span data-ttu-id="7310f-122">È anche possibile passare una tabella appena creata, perché il metodo **merge** crea automaticamente le colonne che utilizza se vengono rilevati conflitti di merge.</span><span class="sxs-lookup"><span data-stu-id="7310f-122">A newly created table can be passed in as well because the **Merge** method automatically creates the columns it uses if merge conflicts are found.</span></span> <span data-ttu-id="7310f-123">Per presentare conflitti di merge vengono utilizzate due colonne.</span><span class="sxs-lookup"><span data-stu-id="7310f-123">Two columns are used to present merge conflicts.</span></span> <span data-ttu-id="7310f-124">La prima colonna è il nome della tabella e la colonna chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="7310f-124">The first column is the table name and the primary key column.</span></span> <span data-ttu-id="7310f-125">La seconda colonna indica il numero di righe della tabella in cui sono presenti errori di Unione.</span><span class="sxs-lookup"><span data-stu-id="7310f-125">The second column is the number of rows of that table that have merge failures.</span></span>

<span data-ttu-id="7310f-126">Se le tabelle con lo stesso nome in entrambi i database non corrispondono al numero di chiavi primarie, ai tipi di colonna, al numero di colonne o ai nomi delle colonne, il metodo **merge** ha esito negativo e invia un messaggio di errore che indica che cosa si è verificato.</span><span class="sxs-lookup"><span data-stu-id="7310f-126">If tables of the same name in both databases do not match in the number of primary keys, the column types, the number of columns, or the column names, the **Merge** method fails and posts an error message stating what occurred.</span></span>

<span data-ttu-id="7310f-127">Affinché la tabella degli errori rimanga, il gestore degli errori deve eseguire il commit del database a cui appartiene la tabella degli errori.</span><span class="sxs-lookup"><span data-stu-id="7310f-127">For the Error table to remain, the error handler must commit the database to which the Error table belongs.</span></span> <span data-ttu-id="7310f-128">Tuttavia, questo commit deve essere eseguito dopo l'utilizzo della terza colonna per ottenere i riferimenti alle tabelle in cui si sono verificati i conflitti di Unione.</span><span class="sxs-lookup"><span data-stu-id="7310f-128">However, this commit should be done after using the third column to obtain the references to those tables where merge conflicts occurred.</span></span>

<span data-ttu-id="7310f-129">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="7310f-129">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7310f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7310f-130">Requirements</span></span>



| <span data-ttu-id="7310f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7310f-131">Requirement</span></span> | <span data-ttu-id="7310f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7310f-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7310f-133">Versione</span><span class="sxs-lookup"><span data-stu-id="7310f-133">Version</span></span><br/> | <span data-ttu-id="7310f-134">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7310f-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7310f-135">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7310f-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7310f-136">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7310f-136">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7310f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7310f-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="7310f-138"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7310f-138"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7310f-139">IID</span><span class="sxs-lookup"><span data-stu-id="7310f-139">IID</span></span><br/>     | <span data-ttu-id="7310f-140">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7310f-140">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




