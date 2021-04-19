---
description: Il metodo di salvataggio permanente dell'oggetto SummaryInfo formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. persevers (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329243"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="52d63-103">SummaryInfo. persevers (metodo)</span><span class="sxs-lookup"><span data-stu-id="52d63-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="52d63-104">Il metodo di **salvataggio permanente** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard.</span><span class="sxs-lookup"><span data-stu-id="52d63-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="52d63-105">Genera un errore se il flusso non può essere scritto correttamente.</span><span class="sxs-lookup"><span data-stu-id="52d63-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="52d63-106">Questo metodo può essere chiamato solo una volta dopo l'impostazione di tutti i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="52d63-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="52d63-107">Le proprietà possono essere ancora lette dopo la scrittura del flusso.</span><span class="sxs-lookup"><span data-stu-id="52d63-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d63-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52d63-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="52d63-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="52d63-109">Parameters</span></span>

<span data-ttu-id="52d63-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="52d63-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52d63-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52d63-111">Return value</span></span>

<span data-ttu-id="52d63-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="52d63-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d63-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52d63-113">Requirements</span></span>



| <span data-ttu-id="52d63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d63-114">Requirement</span></span> | <span data-ttu-id="52d63-115">Valore</span><span class="sxs-lookup"><span data-stu-id="52d63-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d63-116">Versione</span><span class="sxs-lookup"><span data-stu-id="52d63-116">Version</span></span><br/> | <span data-ttu-id="52d63-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52d63-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52d63-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52d63-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52d63-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="52d63-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="52d63-120">DLL</span><span class="sxs-lookup"><span data-stu-id="52d63-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="52d63-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52d63-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="52d63-122">IID</span><span class="sxs-lookup"><span data-stu-id="52d63-122">IID</span></span><br/>     | <span data-ttu-id="52d63-123">IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="52d63-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




