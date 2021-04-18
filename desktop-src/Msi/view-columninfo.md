---
description: La Proprietà ColumnInfo dell'oggetto View restituisce un oggetto record contenente le informazioni richieste su ogni colonna del set di risultati.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Proprietà View. ColumnInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327173"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="87d35-103">Proprietà View. ColumnInfo</span><span class="sxs-lookup"><span data-stu-id="87d35-103">View.ColumnInfo property</span></span>

<span data-ttu-id="87d35-104">La proprietà **ColumnInfo** dell'oggetto [**View**](view-object.md) restituisce un oggetto [**record**](record-object.md) contenente le informazioni richieste su ogni colonna del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="87d35-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="87d35-105">È possibile che vengano richiesti i nomi di colonna o le definizioni delle colonne.</span><span class="sxs-lookup"><span data-stu-id="87d35-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="87d35-106">Le costanti fornite nell'elenco di selezione non hanno nomi.</span><span class="sxs-lookup"><span data-stu-id="87d35-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="87d35-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="87d35-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d35-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87d35-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="87d35-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="87d35-109">Property value</span></span>

<span data-ttu-id="87d35-110">Informazioni necessarie per ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="87d35-110">Required information needed for each column.</span></span>



| <span data-ttu-id="87d35-111">Nome parametro</span><span class="sxs-lookup"><span data-stu-id="87d35-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="87d35-112">Significato</span><span class="sxs-lookup"><span data-stu-id="87d35-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="87d35-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87d35-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="87d35-114">Restituisce i nomi di tutte le colonne non costanti nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="87d35-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="87d35-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="87d35-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="87d35-116">Restituisce i tipi di tutte le colonne non costanti nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="87d35-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87d35-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="87d35-117">Remarks</span></span>

<span data-ttu-id="87d35-118">Le descrizioni delle colonne restituite dalla proprietà **ColumnInfo** sono nel formato descritto in [formato di definizione di colonna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="87d35-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="87d35-119">Ogni colonna è descritta da una stringa nel campo record corrispondente.</span><span class="sxs-lookup"><span data-stu-id="87d35-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="87d35-120">La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri quando applicabile o da altri byte).</span><span class="sxs-lookup"><span data-stu-id="87d35-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="87d35-121">Uno spessore pari a zero indica una larghezza senza limiti (campi di testo lunghi e flussi).</span><span class="sxs-lookup"><span data-stu-id="87d35-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="87d35-122">Una lettera maiuscola indica che nella colonna sono consentiti valori null.</span><span class="sxs-lookup"><span data-stu-id="87d35-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d35-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87d35-123">Requirements</span></span>



| <span data-ttu-id="87d35-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87d35-124">Requirement</span></span> | <span data-ttu-id="87d35-125">Valore</span><span class="sxs-lookup"><span data-stu-id="87d35-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d35-126">Versione</span><span class="sxs-lookup"><span data-stu-id="87d35-126">Version</span></span><br/> | <span data-ttu-id="87d35-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="87d35-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="87d35-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="87d35-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="87d35-129">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="87d35-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="87d35-130">DLL</span><span class="sxs-lookup"><span data-stu-id="87d35-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="87d35-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d35-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="87d35-132">IID</span><span class="sxs-lookup"><span data-stu-id="87d35-132">IID</span></span><br/>     | <span data-ttu-id="87d35-133">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="87d35-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




