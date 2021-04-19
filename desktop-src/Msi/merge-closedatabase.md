---
description: Il metodo ChiudiDatabase dell'oggetto merge chiude il database Windows Installer attualmente aperto.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Metodo merge. ChiudiDatabase (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323988"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="37ac6-103">Merge. ChiudiDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="37ac6-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="37ac6-104">Il metodo **ChiudiDatabase** dell'oggetto [**merge**](merge-object.md) chiude il database Windows Installer attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="37ac6-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ac6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37ac6-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="37ac6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ac6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ac6-107">*bCommit*</span><span class="sxs-lookup"><span data-stu-id="37ac6-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="37ac6-108">**True** se le modifiche devono essere salvate; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="37ac6-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ac6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37ac6-109">Return value</span></span>

<span data-ttu-id="37ac6-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="37ac6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37ac6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ac6-111">Remarks</span></span>

<span data-ttu-id="37ac6-112">La chiusura di un database Cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non sono stati recuperati.</span><span class="sxs-lookup"><span data-stu-id="37ac6-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="37ac6-113">C++</span><span class="sxs-lookup"><span data-stu-id="37ac6-113">C++</span></span>

<span data-ttu-id="37ac6-114">Vedere funzione [**ChiudiDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="37ac6-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ac6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37ac6-115">Requirements</span></span>



| <span data-ttu-id="37ac6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ac6-116">Requirement</span></span> | <span data-ttu-id="37ac6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="37ac6-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ac6-118">Versione</span><span class="sxs-lookup"><span data-stu-id="37ac6-118">Version</span></span><br/> | <span data-ttu-id="37ac6-119">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="37ac6-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="37ac6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37ac6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="37ac6-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="37ac6-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="37ac6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="37ac6-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="37ac6-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ac6-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
