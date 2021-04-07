---
title: Struttura EDB_RSTMAP (ntdsbcli. h)
description: Utilizzato con la funzione DsRestoreRegister per eseguire il mapping di un database di cui è stato eseguito il backup in un nuovo database.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Struttura EDB_RSTMAP Active Directory
- Puntatore alla struttura PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048481"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="69737-105">\_Struttura RSTMAP edb</span><span class="sxs-lookup"><span data-stu-id="69737-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="69737-106">La **struttura \_ RSTMAP di edb** viene utilizzata con la funzione [**DsRestoreRegister**](dsrestoreregister.md) per eseguire il mapping di un database di cui è stato eseguito il backup in un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="69737-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="69737-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69737-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="69737-108">Members</span><span class="sxs-lookup"><span data-stu-id="69737-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="69737-109">**szDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="69737-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="69737-110">Puntatore a una stringa con terminazione null che contiene il nome del database in cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="69737-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="69737-111">**szNewDatabaseName**</span><span class="sxs-lookup"><span data-stu-id="69737-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="69737-112">Puntatore a una stringa con terminazione null che contiene il nuovo nome del database, inclusa la nuova posizione, quando applicabile.</span><span class="sxs-lookup"><span data-stu-id="69737-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69737-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69737-113">Requirements</span></span>



| <span data-ttu-id="69737-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="69737-114">Requirement</span></span> | <span data-ttu-id="69737-115">Valore</span><span class="sxs-lookup"><span data-stu-id="69737-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69737-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69737-116">Minimum supported client</span></span><br/> | <span data-ttu-id="69737-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69737-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="69737-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69737-118">Minimum supported server</span></span><br/> | <span data-ttu-id="69737-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69737-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="69737-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69737-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="69737-121"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="69737-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="69737-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="69737-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="69737-123">**EDB \_ RSTMAPW** (Unicode) e **EDB \_ RSTMAPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="69737-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="69737-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69737-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69737-125">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="69737-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="69737-126">Strutture di backup della directory</span><span class="sxs-lookup"><span data-stu-id="69737-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





