---
description: Imposta i punti degli oggetti attualmente selezionati sull'oggetto dati nei comandi Copy e Cut. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETPOINTS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234087"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="48d45-104">SFVM \_ messaggi di setpoint</span><span class="sxs-lookup"><span data-stu-id="48d45-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="48d45-105">Imposta i punti degli oggetti attualmente selezionati sull'oggetto dati nei comandi **Copy** e **Cut** .</span><span class="sxs-lookup"><span data-stu-id="48d45-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="48d45-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="48d45-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="48d45-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="48d45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48d45-108">*pdtobj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48d45-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="48d45-109">Puntatore a un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> dei comandi **Copy** e **Cut** .</span><span class="sxs-lookup"><span data-stu-id="48d45-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48d45-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48d45-110">Return value</span></span>

<span data-ttu-id="48d45-111">Restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="48d45-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="48d45-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="48d45-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="48d45-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48d45-113">Requirements</span></span>



| <span data-ttu-id="48d45-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48d45-114">Requirement</span></span> | <span data-ttu-id="48d45-115">Valore</span><span class="sxs-lookup"><span data-stu-id="48d45-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48d45-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48d45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48d45-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="48d45-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="48d45-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48d45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48d45-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="48d45-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48d45-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48d45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48d45-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="48d45-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
