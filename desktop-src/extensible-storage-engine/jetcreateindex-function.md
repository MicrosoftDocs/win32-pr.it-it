---
description: 'Altre informazioni su: funzione JetCreateIndex'
title: Funzione JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313104"
---
# <a name="jetcreateindex-function"></a><span data-ttu-id="03b21-103">Funzione JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="03b21-103">JetCreateIndex Function</span></span>


<span data-ttu-id="03b21-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="03b21-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex-function"></a><span data-ttu-id="03b21-105">Funzione JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="03b21-105">JetCreateIndex Function</span></span>

<span data-ttu-id="03b21-106">La funzione **JetCreateIndex** consente di creare un indice di dati in un database Extensible Storage Engine (ESE), che è possibile utilizzare per individuare rapidamente dati specifici.</span><span class="sxs-lookup"><span data-stu-id="03b21-106">The **JetCreateIndex** function enables you to create an index of data in an Extensible Storage Engine (ESE) database, which you can use to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a><span data-ttu-id="03b21-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="03b21-107">Parameters</span></span>

<span data-ttu-id="03b21-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="03b21-108">*sesid*</span></span>

<span data-ttu-id="03b21-109">Contesto della sessione di database da usare per una particolare chiamata API.</span><span class="sxs-lookup"><span data-stu-id="03b21-109">The database session context to use for a particular API call.</span></span>

<span data-ttu-id="03b21-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="03b21-110">*tableid*</span></span>

<span data-ttu-id="03b21-111">Tabella per la quale verrà creato un indice.</span><span class="sxs-lookup"><span data-stu-id="03b21-111">The table that an index will be created for.</span></span>

<span data-ttu-id="03b21-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="03b21-112">*szIndexName*</span></span>

<span data-ttu-id="03b21-113">Puntatore a una stringa con terminazione null che specifica il nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="03b21-113">A pointer to a null-terminated string that specifies the name of the index to be created.</span></span>

<span data-ttu-id="03b21-114">Il nome dell'indice deve essere conforme alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="03b21-114">The index name must conform to the following guidelines:</span></span>

  - <span data-ttu-id="03b21-115">Deve contenere un numero di caratteri inferiore a JET_cbNameMost, escluso il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="03b21-115">It must contain fewer characters than JET_cbNameMost, not including the terminating null character.</span></span>

  - <span data-ttu-id="03b21-116">Deve contenere solo i caratteri delle seguenti categorie: da 0 a 9, da A A Z, da a a z e da tutti i caratteri di punteggiatura, ad eccezione di " \! "</span><span class="sxs-lookup"><span data-stu-id="03b21-116">It must contain only characters from the following categories: 0 through 9, A through Z, a through z, and all punctuation characters except for "\!"</span></span> <span data-ttu-id="03b21-117">(punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero i caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="03b21-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, the ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="03b21-118">Non deve iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="03b21-118">It must not begin with a space.</span></span>

  - <span data-ttu-id="03b21-119">Deve contenere almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="03b21-119">It must contain at least one non-space character.</span></span>

<span data-ttu-id="03b21-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="03b21-120">*grbit*</span></span>

<span data-ttu-id="03b21-121">Gruppo di bit che contiene le opzioni da utilizzare per una particolare chiamata.</span><span class="sxs-lookup"><span data-stu-id="03b21-121">A group of bits that contains the options to be used for a particular call.</span></span> <span data-ttu-id="03b21-122">Questo parametro può includere zero o più opzioni disponibili nella struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="03b21-122">This parameter can include zero or more of the options found in the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="03b21-123">*szKey*</span><span class="sxs-lookup"><span data-stu-id="03b21-123">*szKey*</span></span>

<span data-ttu-id="03b21-124">Puntatore a una doppia stringa con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="03b21-124">A pointer to a double null-terminated string of null-delimited tokens.</span></span>

<span data-ttu-id="03b21-125">Per ulteriori informazioni su questo parametro, vedere la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="03b21-125">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

<span data-ttu-id="03b21-126">*cbKey*</span><span class="sxs-lookup"><span data-stu-id="03b21-126">*cbKey*</span></span>

<span data-ttu-id="03b21-127">Lunghezza, in byte, del parametro *szKey* , inclusi i due caratteri null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="03b21-127">The length, in bytes, of the *szKey* parameter, including the two terminating null characters.</span></span>

<span data-ttu-id="03b21-128">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="03b21-128">*lDensity*</span></span>

<span data-ttu-id="03b21-129">Densità percentuale dell'albero iniziale B + dell'indice.</span><span class="sxs-lookup"><span data-stu-id="03b21-129">The percentage density of the initial index B+ tree.</span></span>

<span data-ttu-id="03b21-130">Per ulteriori informazioni su questo parametro, vedere la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="03b21-130">For more information about this parameter, see the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure.</span></span>

### <a name="return-value"></a><span data-ttu-id="03b21-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03b21-131">Return Value</span></span>

<span data-ttu-id="03b21-132">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="03b21-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="03b21-133">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="03b21-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03b21-134">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="03b21-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="03b21-135">Significato</span><span class="sxs-lookup"><span data-stu-id="03b21-135">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b21-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="03b21-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="03b21-137">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="03b21-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03b21-138">Per un elenco di altri errori che possono essere restituiti dalla funzione **JetCreateIndex** , vedere [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="03b21-138">For a list of additional errors that can be returned by the **JetCreateIndex** function, see [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="03b21-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="03b21-139">Remarks</span></span>

<span data-ttu-id="03b21-140">La chiamata alla funzione **JetCreateIndex** è identica alla chiamata della funzione [JetCreateIndex2](./jetcreateindex2-function.md) con una struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenente le stesse impostazioni dei parametri di **JetCreateIndex** e un parametro *cIndexCreate* uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="03b21-140">Calling the **JetCreateIndex** function is identical to calling the [JetCreateIndex2](./jetcreateindex2-function.md) function with a [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure containing the same settings as the parameters of **JetCreateIndex**, and a *cIndexCreate* parameter equal to 1.</span></span> <span data-ttu-id="03b21-141">Per i campi della struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) che non dispongono di parametri corrispondenti in **JetCreateIndex**, viene utilizzato un valore pari a 0.</span><span class="sxs-lookup"><span data-stu-id="03b21-141">For the fields of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure that do not have corresponding parameters in **JetCreateIndex**, a value of 0 is assumed.</span></span>

<span data-ttu-id="03b21-142">Si noti che **JetCreateIndex** è stato sostituito da [JetCreateIndex2](./jetcreateindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="03b21-142">Note that **JetCreateIndex** has been superseded by [JetCreateIndex2](./jetcreateindex2-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="03b21-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03b21-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03b21-144">Client</span><span class="sxs-lookup"><span data-stu-id="03b21-144">Client</span></span></p></td>
<td><p><span data-ttu-id="03b21-145">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="03b21-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b21-146">Server</span><span class="sxs-lookup"><span data-stu-id="03b21-146">Server</span></span></p></td>
<td><p><span data-ttu-id="03b21-147">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="03b21-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b21-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03b21-148">Header</span></span></p></td>
<td><p><span data-ttu-id="03b21-149">Viene dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="03b21-149">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b21-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="03b21-150">Library</span></span></p></td>
<td><p><span data-ttu-id="03b21-151">USA ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="03b21-151">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03b21-152">DLL</span><span class="sxs-lookup"><span data-stu-id="03b21-152">DLL</span></span></p></td>
<td><p><span data-ttu-id="03b21-153">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="03b21-153">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03b21-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="03b21-154">Unicode</span></span></p></td>
<td><p><span data-ttu-id="03b21-155">Viene implementato come <strong>JetCreateIndexW</strong> (Unicode) e <strong>JetCreateIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="03b21-155">Is implemented as <strong>JetCreateIndexW</strong> (Unicode) and <strong>JetCreateIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="03b21-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03b21-156">See Also</span></span>

[<span data-ttu-id="03b21-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="03b21-157">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="03b21-158">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="03b21-158">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="03b21-159">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="03b21-159">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="03b21-160">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="03b21-160">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="03b21-161">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="03b21-161">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="03b21-162">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="03b21-162">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="03b21-163">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="03b21-163">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="03b21-164">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="03b21-164">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
