---
description: Il metodo commit dell'oggetto di database finalizza il form persistente del database.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Metodo database. commit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331612"
---
# <a name="databasecommit-method"></a><span data-ttu-id="c1f01-103">Metodo database. commit</span><span class="sxs-lookup"><span data-stu-id="c1f01-103">Database.Commit method</span></span>

<span data-ttu-id="c1f01-104">Il metodo **commit** dell'oggetto di [**database**](database-object.md) finalizza il form persistente del database.</span><span class="sxs-lookup"><span data-stu-id="c1f01-104">The **Commit** method of the [**Database**](database-object.md) object finalizes the persistent form of the database.</span></span> <span data-ttu-id="c1f01-105">Tutti i dati persistenti vengono scritti nel database scrivibile e non vengono scritte colonne o righe temporanee.</span><span class="sxs-lookup"><span data-stu-id="c1f01-105">All persistent data is written to the writeable database, and no temporary columns or rows are written.</span></span> <span data-ttu-id="c1f01-106">Questo metodo non ha alcun effetto su un database aperto in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c1f01-106">This method has no effect on a database opened as read-only.</span></span> <span data-ttu-id="c1f01-107">Questo metodo può essere chiamato più volte per salvare lo stato corrente delle tabelle caricate in memoria.</span><span class="sxs-lookup"><span data-stu-id="c1f01-107">This method can be called multiple times to save the current state of tables loaded into memory.</span></span> <span data-ttu-id="c1f01-108">Quando il database viene chiuso, viene eseguito il rollback di tutte le modifiche apportate successivamente all'ultimo **commit** .</span><span class="sxs-lookup"><span data-stu-id="c1f01-108">When the database is finally closed, any changes made subsequent to the last **Commit** are rolled back.</span></span> <span data-ttu-id="c1f01-109">Questo metodo viene in genere chiamato prima dell'arresto quando tutte le modifiche al database sono state finalizzate.</span><span class="sxs-lookup"><span data-stu-id="c1f01-109">This method is normally called prior to shutdown when all database changes have been finalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1f01-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1f01-110">Syntax</span></span>


```JScript
Database.Commit()
```



## <a name="parameters"></a><span data-ttu-id="c1f01-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1f01-111">Parameters</span></span>

<span data-ttu-id="c1f01-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c1f01-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1f01-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1f01-113">Return value</span></span>

<span data-ttu-id="c1f01-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c1f01-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1f01-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1f01-115">Remarks</span></span>

<span data-ttu-id="c1f01-116">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f01-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f01-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1f01-117">Requirements</span></span>



| <span data-ttu-id="c1f01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1f01-118">Requirement</span></span> | <span data-ttu-id="c1f01-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c1f01-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f01-120">Versione</span><span class="sxs-lookup"><span data-stu-id="c1f01-120">Version</span></span><br/> | <span data-ttu-id="c1f01-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1f01-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1f01-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1f01-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1f01-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1f01-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c1f01-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c1f01-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1f01-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1f01-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c1f01-126">IID</span><span class="sxs-lookup"><span data-stu-id="c1f01-126">IID</span></span><br/>     | <span data-ttu-id="c1f01-127">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c1f01-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




