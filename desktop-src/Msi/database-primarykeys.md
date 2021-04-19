---
description: La proprietà PrimaryKeys dell'oggetto di database restituisce un oggetto record contenente il nome della tabella nel campo 0 e i nomi di colonna (che includono le chiavi primarie) nei campi successivi corrispondenti ai numeri di colonna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Proprietà database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333056"
---
# <a name="databaseprimarykeys-property"></a><span data-ttu-id="a3879-103">Proprietà database. PrimaryKeys</span><span class="sxs-lookup"><span data-stu-id="a3879-103">Database.PrimaryKeys property</span></span>

<span data-ttu-id="a3879-104">La proprietà **PrimaryKeys** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**record**](record-object.md) contenente il nome della tabella nel campo 0 e i nomi di colonna (che includono le chiavi primarie) nei campi successivi corrispondenti ai numeri di colonna.</span><span class="sxs-lookup"><span data-stu-id="a3879-104">The **PrimaryKeys** property of the [**Database**](database-object.md) object returns a [**Record**](record-object.md) object containing the table name in field 0 and the column names (comprising the primary keys) in succeeding fields corresponding to their column numbers.</span></span> <span data-ttu-id="a3879-105">Il numero di campi del record è il numero di colonne chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="a3879-105">The field count of the record is the count of primary key columns.</span></span>

<span data-ttu-id="a3879-106">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a3879-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3879-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3879-107">Syntax</span></span>


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a><span data-ttu-id="a3879-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a3879-108">Property value</span></span>

<span data-ttu-id="a3879-109">Nome obbligatorio di una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="a3879-109">Required name of an existing table.</span></span> <span data-ttu-id="a3879-110">Se la tabella non esiste, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="a3879-110">An error is generated if the table does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3879-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3879-111">Remarks</span></span>

<span data-ttu-id="a3879-112">Impossibile utilizzare la proprietà **PrimaryKeys** con [ \_ la tabella Tables o](-tables-table.md) [ \_ Columns](-columns-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3879-112">The **PrimaryKeys** property cannot be used with the [\_Tables table](-tables-table.md) or the [\_Columns table](-columns-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3879-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3879-113">Requirements</span></span>



| <span data-ttu-id="a3879-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3879-114">Requirement</span></span> | <span data-ttu-id="a3879-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a3879-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3879-116">Versione</span><span class="sxs-lookup"><span data-stu-id="a3879-116">Version</span></span><br/> | <span data-ttu-id="a3879-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3879-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a3879-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3879-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a3879-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3879-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a3879-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a3879-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3879-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3879-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a3879-122">IID</span><span class="sxs-lookup"><span data-stu-id="a3879-122">IID</span></span><br/>     | <span data-ttu-id="a3879-123">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a3879-123">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




