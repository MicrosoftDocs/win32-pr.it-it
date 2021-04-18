---
description: 'Altre informazioni su: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317399"
---
# <a name="jet_cbtyp"></a><span data-ttu-id="f27ad-103">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="f27ad-103">JET_CBTYP</span></span>


<span data-ttu-id="f27ad-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f27ad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_cbtyp"></a><span data-ttu-id="f27ad-105">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="f27ad-105">JET_CBTYP</span></span>

<span data-ttu-id="f27ad-106">Il **JET_CBTYP** gruppo di costanti descrive tutti i punti possibili in un'operazione che il motore di database invierà una notifica a un'applicazione chiamando la funzione di CALLBACK di [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f27ad-106">The **JET_CBTYP** group of constants describes all possible points in an operation that the database engine will notify an application by calling the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span> <span data-ttu-id="f27ad-107">Il motore di database passa una di queste costanti nel parametro *cbtyp* della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f27ad-107">The database engine passes one of these constants in the *cbtyp* parameter of the callback function.</span></span> <span data-ttu-id="f27ad-108">Il significato degli altri parametri passati dal motore di database in questa chiamata dipende dalla **JET_CBTYP** specifica passata.</span><span class="sxs-lookup"><span data-stu-id="f27ad-108">The meaning of the other parameters passed by the database engine in this call depend on the specific **JET_CBTYP** passed.</span></span>

<span data-ttu-id="f27ad-109">**Windows XP:**  Il gruppo **JET_CBTYP** di costanti è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f27ad-109">**Windows XP:**  The **JET_CBTYP** group of constants are introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f27ad-110">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="f27ad-110">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="f27ad-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f27ad-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-112">JET_cbtypNull</span><span class="sxs-lookup"><span data-stu-id="f27ad-112">JET_cbtypNull</span></span><br />
<span data-ttu-id="f27ad-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f27ad-113">0x00000000</span></span></p></td>
<td><p><span data-ttu-id="f27ad-114">Questo callback è riservato e sempre considerato non valido.</span><span class="sxs-lookup"><span data-stu-id="f27ad-114">This callback is reserved and always considered invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-115">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="f27ad-115">JET_cbtypFinalize</span></span><br />
<span data-ttu-id="f27ad-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f27ad-116">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="f27ad-117">Questo callback è riservato per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f27ad-117">This callback is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-118">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="f27ad-118">JET_cbtypBeforeInsert</span></span><br />
<span data-ttu-id="f27ad-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f27ad-119">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="f27ad-120">Questo callback si verificherà immediatamente prima dell'inserimento di un nuovo record in una tabella tramite una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-120">This callback will occur just before a new record is inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="f27ad-121">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-121">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-122">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-122">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-123">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-123">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-124"><em>sesid</em>: sessione in cui è presente il record da inserire.</span><span class="sxs-lookup"><span data-stu-id="f27ad-124"><em>sesid</em>: The session that has the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-125"><em>dbid</em>: ID database della tabella che contiene il record da inserire.</span><span class="sxs-lookup"><span data-stu-id="f27ad-125"><em>dbid</em>: The database ID of the table that contains the record to be inserted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-126"><em>TableID</em>: cursore che ha preparato il nuovo record da inserire.</span><span class="sxs-lookup"><span data-stu-id="f27ad-126"><em>tableid</em>: The cursor that has prepared the new record to be inserted.</span></span> <span data-ttu-id="f27ad-127">È importante notare che in questo momento il valore di qualsiasi versione o di colonne con incremento automatico potrebbe non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="f27ad-127">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-128"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-128"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-129"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-129"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-130"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-130"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-131"><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</span><span class="sxs-lookup"><span data-stu-id="f27ad-131"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-132">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="f27ad-132">JET_cbtypAfterInsert</span></span><br />
<span data-ttu-id="f27ad-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f27ad-133">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="f27ad-134">Questo callback si verificherà subito dopo l'inserimento di un nuovo record in una tabella tramite una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a> ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate</a> torni al chiamante.</span><span class="sxs-lookup"><span data-stu-id="f27ad-134">This callback will occur just after a new record has been inserted into a table by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but before <a href="gg269288(v=exchg.10).md">JetUpdate</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="f27ad-135">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-135">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-136">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-136">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-137">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-137">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-138"><em>sesid</em>: la sessione che contiene il record appena inserito.</span><span class="sxs-lookup"><span data-stu-id="f27ad-138"><em>sesid</em>: The session that has the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-139"><em>dbid</em>: ID database della tabella che contiene il record appena inserito.</span><span class="sxs-lookup"><span data-stu-id="f27ad-139"><em>dbid</em>: The database ID of the table that contains the record that was just inserted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-140"><em>TableID</em>: cursore della tabella in cui è stato appena inserito il record.</span><span class="sxs-lookup"><span data-stu-id="f27ad-140"><em>tableid</em>: A cursor on the table into which the record that was just inserted.</span></span> <span data-ttu-id="f27ad-141">Si noti che il cursore è ancora posizionato sulla stessa voce di indice in cui si trovava nel callback di prima dell'inserimento.</span><span class="sxs-lookup"><span data-stu-id="f27ad-141">Note that the cursor is still positioned on the same index entry as it was in the before insert callback.</span></span> <span data-ttu-id="f27ad-142">Si noti inoltre che questa voce di indice potrebbe non essere correlata in alcun modo al record da inserire.</span><span class="sxs-lookup"><span data-stu-id="f27ad-142">Further note that this index entry may not be related in any way to the record being inserted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-143"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-143"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-144"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-144"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-145"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-145"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-146"><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-146"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-147">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="f27ad-147">JET_cbtypBeforeReplace</span></span><br />
<span data-ttu-id="f27ad-148">0x00000008</span><span class="sxs-lookup"><span data-stu-id="f27ad-148">0x00000008</span></span></p></td>
<td><p><span data-ttu-id="f27ad-149">Questo callback si verificherà immediatamente prima di un record esistente in una tabella modificata da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-149">This callback will occur just prior to an existing record in a table being changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</span></span></p>
<p><span data-ttu-id="f27ad-150">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-150">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-151">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-151">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-152">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-152">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-153"><em>sesid</em>: la sessione in cui è presente il record da modificare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-153"><em>sesid</em>: The session that has the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-154"><em>dbid</em>: ID database della tabella che contiene il record da modificare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-154"><em>dbid</em>: The database ID of the table that contains the record to be changed.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-155"><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record da modificare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-155"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be changed.</span></span> <span data-ttu-id="f27ad-156">È importante notare che in questo momento il valore di qualsiasi versione o di colonne con incremento automatico potrebbe non essere corretto.</span><span class="sxs-lookup"><span data-stu-id="f27ad-156">It is important to note that the value of any version or auto-increment columns may not be correct at this time.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-157"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-157"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-158"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-158"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-159"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-159"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-160"><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</span><span class="sxs-lookup"><span data-stu-id="f27ad-160"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-161">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="f27ad-161">JET_cbtypAfterReplace</span></span><br />
<span data-ttu-id="f27ad-162">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f27ad-162">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="f27ad-163">Questo callback si verifica subito dopo la modifica di un record esistente in una tabella da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a> , ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate</a> torni al chiamante.</span><span class="sxs-lookup"><span data-stu-id="f27ad-163">This callback will occur just after an existing record in a table has been changed by a call to <a href="gg269288(v=exchg.10).md">JetUpdate</a> but prior to <a href="gg269288(v=exchg.10).md">JetUpdate</a> returning to its caller.</span></span></p>
<p><span data-ttu-id="f27ad-164">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-164">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-165">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-165">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-166">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-166">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-167"><em>sesid</em>: la sessione che contiene il record appena modificato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-167"><em>sesid</em>: The session that has the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-168"><em>dbid</em>: ID database della tabella che contiene il record appena modificato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-168"><em>dbid</em>: The database ID of the table that contains the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-169"><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record appena modificato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-169"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just changed.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-170"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-170"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-171"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-171"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-172"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-172"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-173"><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-173"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, it will be ignored.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-174">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="f27ad-174">JET_cbtypBeforeDelete</span></span><br />
<span data-ttu-id="f27ad-175">0x00000020</span><span class="sxs-lookup"><span data-stu-id="f27ad-175">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="f27ad-176">Questo callback si verificherà immediatamente prima che un record esistente in una tabella venga eliminato da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-176">This callback will occur just before an existing record in a table is deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a>.</span></span></p>
<p><span data-ttu-id="f27ad-177">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-177">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-178">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-178">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-179">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-179">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-180"><em>sesid</em>: sessione in cui è presente il record da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-180"><em>sesid</em>: The session that has the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-181"><em>dbid</em>: ID database della tabella che contiene il record da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-181"><em>dbid</em>: The database ID of the table that contains the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-182"><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f27ad-182"><em>tableid</em>: A cursor positioned on an index entry associated with the record to be deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-183"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-183"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-184"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-184"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-185"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-185"><em>pvContext</em>: The context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-186"><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</span><span class="sxs-lookup"><span data-stu-id="f27ad-186"><em>ulUnused</em>: <strong>NULL</strong> If an error is returned by the callback, the operation originating the callback will fail with that error.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-187">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="f27ad-187">JET_cbtypAfterDelete</span></span><br />
<span data-ttu-id="f27ad-188">0x00000040</span><span class="sxs-lookup"><span data-stu-id="f27ad-188">0x00000040</span></span></p></td>
<td><p><span data-ttu-id="f27ad-189">Questo callback si verificherà subito dopo l'eliminazione di un record esistente in una tabella da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete</a> ma prima che <a href="gg269315(v=exchg.10).md">JetDelete</a> torni al chiamante.</span><span class="sxs-lookup"><span data-stu-id="f27ad-189">This callback will occur just after an existing record in a table has been deleted by a call to <a href="gg269315(v=exchg.10).md">JetDelete</a> but before <a href="gg269315(v=exchg.10).md">JetDelete</a> returns to its caller.</span></span></p>
<p><span data-ttu-id="f27ad-190">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-190">The function pointer for this callback reason is either passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or is configured at runtime by means of <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span> <span data-ttu-id="f27ad-191">Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-191">For more information, see <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-192">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-192">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-193"><em>sesid</em>: la sessione in cui è stato appena eliminato il record.</span><span class="sxs-lookup"><span data-stu-id="f27ad-193"><em>sesid</em>: The session that has the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-194"><em>dbid</em>: ID database della tabella che contiene il record appena eliminato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-194"><em>dbid</em>: The database ID of the table that contains the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-195"><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record appena eliminato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-195"><em>tableid</em>: A cursor positioned on an index entry associated with the record that was just deleted.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-196"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-196"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-197"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-197"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-198"><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-198"><em>pvContext</em>: the context pointer passed to <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> or <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-199"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-199"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="f27ad-200">Se un errore viene restituito dal callback, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-200">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-201">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="f27ad-201">JET_cbtypUserDefinedDefaultValue</span></span><br />
<span data-ttu-id="f27ad-202">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f27ad-202">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="f27ad-203">Questo callback si verifica quando il motore deve recuperare il valore predefinito definito dall'utente di una colonna dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f27ad-203">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="f27ad-204">Questo callback è essenzialmente un'implementazione limitata di <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> valutata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f27ad-204">This callback is essentially a limited implementation of <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> that is evaluated by the application.</span></span> <span data-ttu-id="f27ad-205">Per un valore predefinito definito dall'utente può essere restituito un massimo di un valore di colonna.</span><span class="sxs-lookup"><span data-stu-id="f27ad-205">A maximum of one column value can be returned for a user defined default value.</span></span></p>
<p><span data-ttu-id="f27ad-206">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg294122(v=exchg.10).md">JetAddColumn</a> per mezzo di una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> o passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> in una struttura di <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> in una struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f27ad-206">The function pointer for this callback reason is either passed to <a href="gg294122(v=exchg.10).md">JetAddColumn</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure or passed to <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> by means of a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure in a <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure in a <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure.</span></span></p>
<p><span data-ttu-id="f27ad-207">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-207">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-208"><em>sesid</em>: la sessione che sta calcolando il valore predefinito definito dall'utente</span><span class="sxs-lookup"><span data-stu-id="f27ad-208"><em>sesid</em>: The session that is computing the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="f27ad-209"><em>dbid</em>: ID database della tabella che contiene il valore predefinito definito dall'utente</span><span class="sxs-lookup"><span data-stu-id="f27ad-209"><em>dbid</em>: The database ID of the table that contains the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="f27ad-210"><em>TableID</em>: cursore posizionato sul record per il quale viene recuperato il valore predefinito definito dall'utente</span><span class="sxs-lookup"><span data-stu-id="f27ad-210"><em>tableid</em>: A cursor positioned on the record for which the user defined default value is being retrieved</span></span></p></li>
<li><p><span data-ttu-id="f27ad-211"><em>pvArg1</em>: buffer di output per il valore predefinito definito dall'utente</span><span class="sxs-lookup"><span data-stu-id="f27ad-211"><em>pvArg1</em>: The output buffer for the user defined default value</span></span></p></li>
<li><p><span data-ttu-id="f27ad-212"><em>pvArg2</em>: in input, si tratta della dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="f27ad-212"><em>pvArg2</em>: On input, this is the size of the output buffer.</span></span> <span data-ttu-id="f27ad-213">Nell'output corrisponde alla dimensione effettiva del valore predefinito definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f27ad-213">On output, this is the actual size of the user defined default value.</span></span> <span data-ttu-id="f27ad-214">in entrambi i casi, la dimensione è una Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f27ad-214">in either case, the size is a 32-bit unsigned integer.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-215"><em>pvContext</em>: puntatore a un buffer contenente i dati utente specificati nella struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> quando è stata creata la colonna oppure null se non è stato specificato alcun contesto.</span><span class="sxs-lookup"><span data-stu-id="f27ad-215"><em>pvContext</em>: A pointer to a buffer containing the user data specified in the <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure when the column was created or NULL if no context was provided.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-216"><em>ulUnused</em>: ID di colonna della colonna per cui viene recuperato il valore predefinito definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f27ad-216"><em>ulUnused</em>: The column ID of the column for which the user defined default value is being retrieved.</span></span></p></li>
</ul>
<p><span data-ttu-id="f27ad-217">Se viene restituito un errore dal callback, l'operazione di origine del callback avrà esito negativo con l'errore.</span><span class="sxs-lookup"><span data-stu-id="f27ad-217">If an error is returned by the callback then the operation originating the callback will fail with that error.</span></span></p>
<p><span data-ttu-id="f27ad-218">Se JET_wrnBufferTruncated viene restituito dal callback, l'operazione continuerà, ma l'intero valore non viene recuperato durante il callback.</span><span class="sxs-lookup"><span data-stu-id="f27ad-218">If JET_wrnBufferTruncated is returned by the callback, the operation will continue, but the entire value is not retrieved during the callback.</span></span></p>
<p><span data-ttu-id="f27ad-219">Se JET_wrnColumnNull viene restituito dal callback, l'operazione continuerà, ma il valore predefinito definito dall'utente per la colonna è NULL.</span><span class="sxs-lookup"><span data-stu-id="f27ad-219">If JET_wrnColumnNull is returned by the callback, the operation will continue, but the user defined default value for the column is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-220">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="f27ad-220">JET_cbtypOnlineDefragCompleted</span></span><br />
<span data-ttu-id="f27ad-221">0x00000100</span><span class="sxs-lookup"><span data-stu-id="f27ad-221">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="f27ad-222">Questo callback si verifica quando la deframmentazione in linea di un database iniziata da <a href="gg269317(v=exchg.10).md">JetDefragment</a> è stata interrotta a causa del completamento del processo o del raggiungimento del limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="f27ad-222">This callback will occur when the online defragmentation of a database as initiated by <a href="gg269317(v=exchg.10).md">JetDefragment</a> has stopped due to either the process being completed or the time limit being reached.</span></span></p>
<p><span data-ttu-id="f27ad-223">Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-223">The function pointer for this callback reason is passed to <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span> <span data-ttu-id="f27ad-224">Per ulteriori informazioni, vedere <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-224">For more information, see <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</span></span></p>
<p><span data-ttu-id="f27ad-225">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-225">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-226"><em>sesid</em>: sessione utilizzata per eseguire la deframmentazione in linea del database o JET_sesidNil per un file di streaming.</span><span class="sxs-lookup"><span data-stu-id="f27ad-226"><em>sesid</em>: The session used to perform online defragmentation for the database or JET_sesidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-227"><em>dbid</em>: ID del database da deframmentare o JET_dbidNil per un file di streaming.</span><span class="sxs-lookup"><span data-stu-id="f27ad-227"><em>dbid</em>: The database ID of the database being defragmented or JET_dbidNil for a streaming file.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-228"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-228"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-229"><em>pvArg1</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-229"><em>pvArg1</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-230"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-230"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-231"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-231"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-232"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-232"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="f27ad-233">Se un errore viene restituito dal callback, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-233">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-234">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="f27ad-234">JET_cbtypFreeCursorLS</span></span><br />
<span data-ttu-id="f27ad-235">0x00000200</span><span class="sxs-lookup"><span data-stu-id="f27ad-235">0x00000200</span></span></p></td>
<td><p><span data-ttu-id="f27ad-236">Questo callback si verifica quando l'applicazione deve eseguire la pulizia dell'handle di contesto per l'archiviazione locale associata a un cursore rilasciato dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="f27ad-236">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="f27ad-237">Per ulteriori informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-237">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="f27ad-238">Il puntatore a funzione per questo motivo di callback viene configurato per mezzo di <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-238">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-239">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-239">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-240"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-240"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-241"><em>dbid</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-241"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-242"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-242"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-243"><em>pvArg1</em>: set di handle di contesto con <a href="gg269243(v=exchg.10).md">JetSetLS</a></span><span class="sxs-lookup"><span data-stu-id="f27ad-243"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a></span></span></p></li>
<li><p><span data-ttu-id="f27ad-244"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-244"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-245"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-245"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-246"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-246"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="f27ad-247">Se un errore viene restituito dal callback, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-247">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-248">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="f27ad-248">JET_cbtypFreeTableLS</span></span><br />
<span data-ttu-id="f27ad-249">0x00000400</span><span class="sxs-lookup"><span data-stu-id="f27ad-249">0x00000400</span></span></p></td>
<td><p><span data-ttu-id="f27ad-250">Questo callback si verificherà come il risultato della necessità che l'applicazione ripulisca l'handle di contesto per l'archiviazione locale associata a una tabella rilasciata dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="f27ad-250">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="f27ad-251">Per ulteriori informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-251">For more information, see <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p>
<p><span data-ttu-id="f27ad-252">Il puntatore a funzione per questo motivo di callback viene configurato per mezzo di <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-252">The function pointer for this callback reason is configured by means of <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</span></span></p>
<p><span data-ttu-id="f27ad-253">I parametri di callback avranno i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f27ad-253">The callback parameters will have the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="f27ad-254"><em>sesid</em>: JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-254"><em>sesid</em>: JET_sesidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-255"><em>dbid</em>: JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-255"><em>dbid</em>: JET_dbidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-256"><em>TableID</em>: JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="f27ad-256"><em>tableid</em>: JET_tableidNil</span></span></p></li>
<li><p><span data-ttu-id="f27ad-257"><em>pvArg1</em>: set di handle di contesto con <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span><span class="sxs-lookup"><span data-stu-id="f27ad-257"><em>pvArg1</em>: The context handle set using <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</span></span></p></li>
<li><p><span data-ttu-id="f27ad-258"><em>pvArg2</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-258"><em>pvArg2</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-259"><em>pvContext</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-259"><em>pvContext</em>: <strong>NULL</strong></span></span></p></li>
<li><p><span data-ttu-id="f27ad-260"><em>ulUnused</em>: <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-260"><em>ulUnused</em>: <strong>NULL</strong></span></span></p></li>
</ul>
<p><span data-ttu-id="f27ad-261">Se un errore viene restituito dal callback, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f27ad-261">If an error is returned by the callback, it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f27ad-262">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f27ad-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f27ad-264">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f27ad-264">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f27ad-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f27ad-266">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f27ad-266">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f27ad-267"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f27ad-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f27ad-268">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f27ad-268">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f27ad-269">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f27ad-269">See Also</span></span>

[<span data-ttu-id="f27ad-270">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f27ad-270">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)
