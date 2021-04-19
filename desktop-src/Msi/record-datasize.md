---
description: La proprietà DataSize dell'oggetto record è una proprietà di sola lettura che restituisce la dimensione dei dati per il campo designato.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Proprietà record. DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328772"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="a17e2-103">Proprietà record. DataSize</span><span class="sxs-lookup"><span data-stu-id="a17e2-103">Record.DataSize property</span></span>

<span data-ttu-id="a17e2-104">La proprietà **DataSize** dell'oggetto [**record**](record-object.md) è una proprietà di sola lettura che restituisce la dimensione dei dati per il campo designato.</span><span class="sxs-lookup"><span data-stu-id="a17e2-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="a17e2-105">Se i dati sono un flusso, viene restituita la lunghezza del flusso in byte.</span><span class="sxs-lookup"><span data-stu-id="a17e2-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="a17e2-106">Se i dati sono una stringa, viene restituita la lunghezza della stringa senza null.</span><span class="sxs-lookup"><span data-stu-id="a17e2-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="a17e2-107">Se i dati sono di tipo Integer, viene restituito il valore 4 (che indica le dimensioni dell'Integer).</span><span class="sxs-lookup"><span data-stu-id="a17e2-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="a17e2-108">Se i dati sono null, viene restituito 0.</span><span class="sxs-lookup"><span data-stu-id="a17e2-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="a17e2-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a17e2-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17e2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a17e2-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="a17e2-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a17e2-111">Property value</span></span>

<span data-ttu-id="a17e2-112">Numero di campo obbligatorio del valore all'interno del record, basato su 1.</span><span class="sxs-lookup"><span data-stu-id="a17e2-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="a17e2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a17e2-113">Requirements</span></span>



| <span data-ttu-id="a17e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a17e2-114">Requirement</span></span> | <span data-ttu-id="a17e2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a17e2-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a17e2-116">Versione</span><span class="sxs-lookup"><span data-stu-id="a17e2-116">Version</span></span><br/> | <span data-ttu-id="a17e2-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a17e2-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a17e2-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a17e2-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a17e2-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="a17e2-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a17e2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a17e2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a17e2-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17e2-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a17e2-122">IID</span><span class="sxs-lookup"><span data-stu-id="a17e2-122">IID</span></span><br/>     | <span data-ttu-id="a17e2-123">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a17e2-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




