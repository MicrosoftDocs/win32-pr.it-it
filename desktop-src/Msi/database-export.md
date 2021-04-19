---
description: Il metodo Export dell'oggetto di database copia la struttura e i dati da una tabella specificata in un file di archivio di testo.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Metodo database. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326544"
---
# <a name="databaseexport-method"></a><span data-ttu-id="c2cec-103">Metodo database. Export</span><span class="sxs-lookup"><span data-stu-id="c2cec-103">Database.Export method</span></span>

<span data-ttu-id="c2cec-104">Il metodo **Export** dell'oggetto di [**database**](database-object.md) copia la struttura e i dati da una tabella specificata in un file di [Archivio di testo](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="c2cec-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2cec-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="c2cec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2cec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2cec-107">*tabella*</span><span class="sxs-lookup"><span data-stu-id="c2cec-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cec-108">Nome obbligatorio della tabella di database.</span><span class="sxs-lookup"><span data-stu-id="c2cec-108">Required name of the database table.</span></span> <span data-ttu-id="c2cec-109">Distinzione tra maiuscole e minuscole se si usa il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="c2cec-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="c2cec-110">*path*</span><span class="sxs-lookup"><span data-stu-id="c2cec-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cec-111">Stringa obbligatoria che rappresenta il percorso della cartella in cui è inserito il file di testo.</span><span class="sxs-lookup"><span data-stu-id="c2cec-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="c2cec-112">*file*</span><span class="sxs-lookup"><span data-stu-id="c2cec-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="c2cec-113">Nome obbligatorio del file da creare.</span><span class="sxs-lookup"><span data-stu-id="c2cec-113">Required name of the file to be created.</span></span> <span data-ttu-id="c2cec-114">Questa operazione non include la cartella, che deve essere impostata nell'oggetto Path.</span><span class="sxs-lookup"><span data-stu-id="c2cec-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2cec-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2cec-115">Return value</span></span>

<span data-ttu-id="c2cec-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c2cec-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cec-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2cec-117">Remarks</span></span>

<span data-ttu-id="c2cec-118">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c2cec-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2cec-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2cec-119">Requirements</span></span>



| <span data-ttu-id="c2cec-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2cec-120">Requirement</span></span> | <span data-ttu-id="c2cec-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c2cec-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2cec-122">Versione</span><span class="sxs-lookup"><span data-stu-id="c2cec-122">Version</span></span><br/> | <span data-ttu-id="c2cec-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c2cec-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c2cec-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c2cec-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c2cec-125">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2cec-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c2cec-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c2cec-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c2cec-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2cec-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c2cec-128">IID</span><span class="sxs-lookup"><span data-stu-id="c2cec-128">IID</span></span><br/>     | <span data-ttu-id="c2cec-129">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c2cec-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




