---
description: Il metodo ReadStream dell'oggetto record legge un numero specificato di byte da un campo record che contiene dati di flusso.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Metodo record. ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328766"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="3f79f-103">Metodo record. ReadStream</span><span class="sxs-lookup"><span data-stu-id="3f79f-103">Record.ReadStream method</span></span>

<span data-ttu-id="3f79f-104">Il metodo **ReadStream** dell'oggetto [**record**](record-object.md) legge un numero specificato di byte da un campo record che contiene dati di flusso.</span><span class="sxs-lookup"><span data-stu-id="3f79f-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f79f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f79f-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="3f79f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f79f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f79f-107">*campo*</span><span class="sxs-lookup"><span data-stu-id="3f79f-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="3f79f-108">Il numero di campo obbligatorio del valore all'interno del record, basato su 1.</span><span class="sxs-lookup"><span data-stu-id="3f79f-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="3f79f-109">*length*</span><span class="sxs-lookup"><span data-stu-id="3f79f-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="3f79f-110">Numero necessario di byte da leggere dal flusso.</span><span class="sxs-lookup"><span data-stu-id="3f79f-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="3f79f-111">*format*</span><span class="sxs-lookup"><span data-stu-id="3f79f-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="3f79f-112">Interpretazione richiesta e restituzione dei byte di dati.</span><span class="sxs-lookup"><span data-stu-id="3f79f-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="3f79f-113">Nome parametro</span><span class="sxs-lookup"><span data-stu-id="3f79f-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="3f79f-114">Significato</span><span class="sxs-lookup"><span data-stu-id="3f79f-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="3f79f-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f79f-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3f79f-116">Come Long Integer, la lunghezza deve essere compresa tra 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="3f79f-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="3f79f-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3f79f-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="3f79f-118">Dati come **BSTR**, ovvero un byte per carattere.</span><span class="sxs-lookup"><span data-stu-id="3f79f-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="3f79f-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3f79f-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="3f79f-120">Byte ANSI convertiti in un **BSTR** Unicode.</span><span class="sxs-lookup"><span data-stu-id="3f79f-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="3f79f-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3f79f-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="3f79f-122">Coppie di byte restituite direttamente come **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="3f79f-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f79f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f79f-123">Return value</span></span>

<span data-ttu-id="3f79f-124">Questo metodo restituisce una stringa che contiene il numero di byte richiesto letti da un campo di record.</span><span class="sxs-lookup"><span data-stu-id="3f79f-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f79f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f79f-125">Remarks</span></span>

<span data-ttu-id="3f79f-126">Il valore restituito di un campo inesistente è un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="3f79f-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="3f79f-127">Se il flusso ha un minor numero di byte richiesti dal conteggio, la stringa restituita viene abbreviata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="3f79f-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="3f79f-128">Per un esempio di questo metodo, vedere [copiare il file ANSI in un campo del database](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="3f79f-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f79f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f79f-129">Requirements</span></span>



| <span data-ttu-id="3f79f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f79f-130">Requirement</span></span> | <span data-ttu-id="3f79f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3f79f-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f79f-132">Versione</span><span class="sxs-lookup"><span data-stu-id="3f79f-132">Version</span></span><br/> | <span data-ttu-id="3f79f-133">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f79f-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3f79f-134">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3f79f-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3f79f-135">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f79f-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3f79f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3f79f-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f79f-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f79f-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3f79f-138">IID</span><span class="sxs-lookup"><span data-stu-id="3f79f-138">IID</span></span><br/>     | <span data-ttu-id="3f79f-139">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3f79f-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




