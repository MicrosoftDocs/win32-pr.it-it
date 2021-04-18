---
description: Il metodo sestream dell'oggetto record copia il contenuto del file specificato nel campo record designato come dati di flusso. Non è possibile inserire i dati del flusso in campi temporanei.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Metodo record. sestream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330920"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="837a2-104">Metodo record. sestream</span><span class="sxs-lookup"><span data-stu-id="837a2-104">Record.SetStream method</span></span>

<span data-ttu-id="837a2-105">Il metodo **sestream** dell'oggetto [**record**](record-object.md) copia il contenuto del file specificato nel campo record designato come dati di flusso.</span><span class="sxs-lookup"><span data-stu-id="837a2-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="837a2-106">Non è possibile inserire i dati del flusso in campi temporanei.</span><span class="sxs-lookup"><span data-stu-id="837a2-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="837a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="837a2-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="837a2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="837a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="837a2-109">*campo*</span><span class="sxs-lookup"><span data-stu-id="837a2-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="837a2-110">Numero di campo obbligatorio del valore all'interno del record, basato su 1.</span><span class="sxs-lookup"><span data-stu-id="837a2-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="837a2-111">*filePath*</span><span class="sxs-lookup"><span data-stu-id="837a2-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="837a2-112">Percorso del file da copiare.</span><span class="sxs-lookup"><span data-stu-id="837a2-112">The location of the file to copy.</span></span> <span data-ttu-id="837a2-113">Non viene eseguita alcuna conversione di alcun tipo.</span><span class="sxs-lookup"><span data-stu-id="837a2-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="837a2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="837a2-114">Return value</span></span>

<span data-ttu-id="837a2-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="837a2-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="837a2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="837a2-116">Remarks</span></span>

<span data-ttu-id="837a2-117">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="837a2-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="837a2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="837a2-118">Requirements</span></span>



| <span data-ttu-id="837a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="837a2-119">Requirement</span></span> | <span data-ttu-id="837a2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="837a2-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837a2-121">Versione</span><span class="sxs-lookup"><span data-stu-id="837a2-121">Version</span></span><br/> | <span data-ttu-id="837a2-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="837a2-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="837a2-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="837a2-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="837a2-124">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="837a2-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="837a2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="837a2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="837a2-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837a2-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="837a2-127">IID</span><span class="sxs-lookup"><span data-stu-id="837a2-127">IID</span></span><br/>     | <span data-ttu-id="837a2-128">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="837a2-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




