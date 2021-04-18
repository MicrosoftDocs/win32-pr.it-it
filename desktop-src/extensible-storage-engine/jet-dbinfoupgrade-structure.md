---
description: 'Altre informazioni su: struttura JET_DBINFOUPGRADE'
title: Struttura JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306831"
---
# <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="3ed2c-103">Struttura JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="3ed2c-103">JET_DBINFOUPGRADE Structure</span></span>


<span data-ttu-id="3ed2c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3ed2c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfoupgrade-structure"></a><span data-ttu-id="3ed2c-105">Struttura JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="3ed2c-105">JET_DBINFOUPGRADE Structure</span></span>

<span data-ttu-id="3ed2c-106">La struttura **JET_DBINFOUPGRADE** include informazioni sullo stato di aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-106">The **JET_DBINFOUPGRADE** structure holds information about the upgrade status of the database.</span></span> <span data-ttu-id="3ed2c-107">Questo valore viene recuperato solo se **JET_DBINFOUPGRADE** è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3ed2c-107">This value is retrieved only if **JET_DBINFOUPGRADE** was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="3ed2c-108">Questa struttura non è necessaria per le versioni correnti del sistema operativo del motore di database.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-108">This structure is not required for current operating system versions of the database engine.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a><span data-ttu-id="3ed2c-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3ed2c-109">Members</span></span>

<span data-ttu-id="3ed2c-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-110">**cbStruct**</span></span>

<span data-ttu-id="3ed2c-111">Impostare sulla dimensione della struttura di **JET_DBINFOUPGRADE** , in byte.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-111">Set to the size of the **JET_DBINFOUPGRADE** structure, in bytes.</span></span>

<span data-ttu-id="3ed2c-112">**cbFilesizeLow**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-112">**cbFilesizeLow**</span></span>

<span data-ttu-id="3ed2c-113">**DWORD** basso che riflette le dimensioni correnti del file per il database.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-113">The low **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="3ed2c-114">**cbFilesizeHigh**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-114">**cbFilesizeHigh**</span></span>

<span data-ttu-id="3ed2c-115">**Valore DWORD** elevato che rispecchia le dimensioni correnti del file per il database.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-115">The high **DWORD** that reflects the current file size for the database.</span></span>

<span data-ttu-id="3ed2c-116">**cbFreeSpaceRequiredLow**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-116">**cbFreeSpaceRequiredLow**</span></span>

<span data-ttu-id="3ed2c-117">Il **valore DWORD** basso dello spazio disponibile su disco stimato necessario per un aggiornamento sul posto.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-117">The low **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="3ed2c-118">**cbFreeSpaceRequiredHigh**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-118">**cbFreeSpaceRequiredHigh**</span></span>

<span data-ttu-id="3ed2c-119">**Valore DWORD** alto dello spazio disponibile su disco stimato necessario per un aggiornamento sul posto.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-119">The high **DWORD** of estimated free disk space required for an in-place upgrade.</span></span>

<span data-ttu-id="3ed2c-120">**csecToUpgrade**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-120">**csecToUpgrade**</span></span>

<span data-ttu-id="3ed2c-121">Tempo stimato necessario per l'aggiornamento, in secondi.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-121">The estimated time required to upgrade, in seconds.</span></span>

<span data-ttu-id="3ed2c-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-122">**ulFlags**</span></span>

<span data-ttu-id="3ed2c-123">Un campo di bit è costituito da zero o più dei flag seguenti: **fUpgradable**, **fAlreadyUpgraded**.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-123">A bit field made of zero or more of the following flags: **fUpgradable**, **fAlreadyUpgraded**.</span></span>

<span data-ttu-id="3ed2c-124">**fUpgradable**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-124">**fUpgradable**</span></span>

<span data-ttu-id="3ed2c-125">Il database è aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-125">The database is upgradeable.</span></span>

<span data-ttu-id="3ed2c-126">**fAlreadyUpgraded**</span><span class="sxs-lookup"><span data-stu-id="3ed2c-126">**fAlreadyUpgraded**</span></span>

<span data-ttu-id="3ed2c-127">Il database viene aggiornato al formato del database corrente.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-127">The database is upgraded to the current database format.</span></span>

### <a name="remarks"></a><span data-ttu-id="3ed2c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ed2c-128">Remarks</span></span>

<span data-ttu-id="3ed2c-129">Una struttura **JET_DBINFOUPGRADE** viene popolata da una chiamata a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="3ed2c-129">A **JET_DBINFOUPGRADE** structure is populated by a call to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span> <span data-ttu-id="3ed2c-130">Se la funzione ha esito negativo, il contenuto della struttura non è definito.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-130">If the function does not succeed, the contents of the structure are undefined.</span></span>

### <a name="requirements"></a><span data-ttu-id="3ed2c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ed2c-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ed2c-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3ed2c-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed2c-133">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ed2c-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3ed2c-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed2c-135">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ed2c-136"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3ed2c-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed2c-137">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3ed2c-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3ed2c-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3ed2c-138">See Also</span></span>

[<span data-ttu-id="3ed2c-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3ed2c-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3ed2c-140">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3ed2c-140">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3ed2c-141">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3ed2c-141">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3ed2c-142">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3ed2c-142">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3ed2c-143">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3ed2c-143">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="3ed2c-144">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="3ed2c-144">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="3ed2c-145">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="3ed2c-145">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="3ed2c-146">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="3ed2c-146">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
