---
description: La proprietà DatabaseState dell'oggetto di database è una proprietà di sola lettura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Proprietà database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326545"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="07b52-103">Proprietà database. DatabaseState</span><span class="sxs-lookup"><span data-stu-id="07b52-103">Database.DatabaseState property</span></span>

<span data-ttu-id="07b52-104">La proprietà **DatabaseState** dell'oggetto di [**database**](database-object.md) è una proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07b52-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="07b52-105">Questa proprietà restituisce lo stato di persistenza del database come uno dei parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="07b52-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="07b52-106">Stato del database</span><span class="sxs-lookup"><span data-stu-id="07b52-106">Database state</span></span>        | <span data-ttu-id="07b52-107">Valore</span><span class="sxs-lookup"><span data-stu-id="07b52-107">Value</span></span> | <span data-ttu-id="07b52-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07b52-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b52-109">msiDatabaseStateRead</span><span class="sxs-lookup"><span data-stu-id="07b52-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="07b52-110">0</span><span class="sxs-lookup"><span data-stu-id="07b52-110">0</span></span>     | <span data-ttu-id="07b52-111">Il database viene aperto in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07b52-111">Database opens as read-only.</span></span> <span data-ttu-id="07b52-112">Le modifiche ai dati persistenti non sono consentite e i dati temporanei non vengono salvati.</span><span class="sxs-lookup"><span data-stu-id="07b52-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="07b52-113">msiDatabaseStateWrite</span><span class="sxs-lookup"><span data-stu-id="07b52-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="07b52-114">1</span><span class="sxs-lookup"><span data-stu-id="07b52-114">1</span></span>     | <span data-ttu-id="07b52-115">Il database è completamente operativo per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="07b52-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="07b52-116">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07b52-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b52-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07b52-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="07b52-118">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="07b52-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="07b52-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07b52-119">Requirements</span></span>



| <span data-ttu-id="07b52-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b52-120">Requirement</span></span> | <span data-ttu-id="07b52-121">Valore</span><span class="sxs-lookup"><span data-stu-id="07b52-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b52-122">Versione</span><span class="sxs-lookup"><span data-stu-id="07b52-122">Version</span></span><br/> | <span data-ttu-id="07b52-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07b52-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="07b52-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07b52-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="07b52-125">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="07b52-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="07b52-126">DLL</span><span class="sxs-lookup"><span data-stu-id="07b52-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="07b52-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b52-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="07b52-128">IID</span><span class="sxs-lookup"><span data-stu-id="07b52-128">IID</span></span><br/>     | <span data-ttu-id="07b52-129">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="07b52-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




