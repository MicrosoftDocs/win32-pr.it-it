---
description: Il metodo Import dell'oggetto di database importa una tabella di database da un file di archivio di testo, eliminando tutte le tabelle esistenti.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Metodo database. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327663"
---
# <a name="databaseimport-method"></a><span data-ttu-id="a5e42-103">Metodo database. Import</span><span class="sxs-lookup"><span data-stu-id="a5e42-103">Database.Import method</span></span>

<span data-ttu-id="a5e42-104">Il metodo **Import** dell'oggetto di [**database**](database-object.md) importa una tabella di database da un file di [Archivio di testo](text-archive-files.md), eliminando tutte le tabelle esistenti.</span><span class="sxs-lookup"><span data-stu-id="a5e42-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5e42-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="a5e42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5e42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e42-107">*path*</span><span class="sxs-lookup"><span data-stu-id="a5e42-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="a5e42-108">Cartella obbligatoria in cui è presente il file di testo.</span><span class="sxs-lookup"><span data-stu-id="a5e42-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="a5e42-109">*file*</span><span class="sxs-lookup"><span data-stu-id="a5e42-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="a5e42-110">Nome obbligatorio del file da importare.</span><span class="sxs-lookup"><span data-stu-id="a5e42-110">Required name of the file to be imported.</span></span> <span data-ttu-id="a5e42-111">Questa operazione non include la cartella, che deve essere impostata nell'oggetto Path.</span><span class="sxs-lookup"><span data-stu-id="a5e42-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="a5e42-112">Il nome della tabella viene specificato all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="a5e42-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e42-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5e42-113">Return value</span></span>

<span data-ttu-id="a5e42-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a5e42-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e42-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5e42-115">Remarks</span></span>

<span data-ttu-id="a5e42-116">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="a5e42-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e42-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5e42-117">Requirements</span></span>



| <span data-ttu-id="a5e42-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5e42-118">Requirement</span></span> | <span data-ttu-id="a5e42-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a5e42-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e42-120">Versione</span><span class="sxs-lookup"><span data-stu-id="a5e42-120">Version</span></span><br/> | <span data-ttu-id="a5e42-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a5e42-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a5e42-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5e42-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a5e42-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5e42-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a5e42-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a5e42-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a5e42-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e42-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a5e42-126">IID</span><span class="sxs-lookup"><span data-stu-id="a5e42-126">IID</span></span><br/>     | <span data-ttu-id="a5e42-127">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a5e42-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a5e42-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5e42-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e42-129">**Database**</span><span class="sxs-lookup"><span data-stu-id="a5e42-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="a5e42-130">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="a5e42-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




