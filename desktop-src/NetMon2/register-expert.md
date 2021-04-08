---
description: L'esperto deve implementare la funzione Register Expert. Network Monitor chiama la funzione Register Expert per ottenere informazioni sull'esperto.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Funzione Register Expert callback (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880706"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="9eb8f-104">Registra funzione di callback esperto</span><span class="sxs-lookup"><span data-stu-id="9eb8f-104">Register Expert callback function</span></span>

<span data-ttu-id="9eb8f-105">L'esperto deve implementare la funzione **Register** Expert.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="9eb8f-106">Network Monitor chiama la funzione **Register** Expert per ottenere informazioni sull'esperto.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb8f-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9eb8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eb8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb8f-109">*pExpertInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9eb8f-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb8f-110">Puntatore a una struttura [**EXPERTENUMINFO**](expertenuminfo.md) che Network Monitor alloca.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="9eb8f-111">L'esperto compila la struttura con tutte le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb8f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eb8f-112">Return value</span></span>

<span data-ttu-id="9eb8f-113">Se la funzione ha esito positivo, il valore restituito è **true** e la funzione restituisce le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="9eb8f-114">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb8f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eb8f-115">Remarks</span></span>

<span data-ttu-id="9eb8f-116">Il membro della **versione** della struttura [**EXPERTENUMINFO**](expertenuminfo.md) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9eb8f-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb8f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb8f-117">Requirements</span></span>



| <span data-ttu-id="9eb8f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb8f-118">Requirement</span></span> | <span data-ttu-id="9eb8f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb8f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb8f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb8f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb8f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9eb8f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9eb8f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb8f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb8f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9eb8f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9eb8f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eb8f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb8f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb8f-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




