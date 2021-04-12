---
title: Unione RAS_PARAMS_VALUE (rassapi. h)
description: L' \_ Unione del valore params RAS \_ viene utilizzata nella \_ struttura dei parametri RAS per archiviare i dati associati a un parametro specifico del supporto.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS Unione RAS_PARAMS_VALUE
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118938"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="26641-104">\_Unione valore params RAS \_</span><span class="sxs-lookup"><span data-stu-id="26641-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="26641-105">\[L'Unione del **\_ \_ valore params RAS** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="26641-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="26641-106">L'Unione del **\_ \_ valore params RAS** viene utilizzata nella struttura dei [**\_ parametri RAS**](ras-parameters-str.md) per archiviare i dati associati a un parametro specifico del supporto.</span><span class="sxs-lookup"><span data-stu-id="26641-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="26641-107">Il membro di **\_ tipo P** della struttura dei **\_ parametri RAS** usa un valore dell'enumerazione del [**\_ \_ formato params RAS**](ras-params-format-str.md) per indicare il tipo di valore attualmente archiviato **nel \_ \_ valore params RAS**.</span><span class="sxs-lookup"><span data-stu-id="26641-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="26641-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26641-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="26641-109">Members</span><span class="sxs-lookup"><span data-stu-id="26641-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="26641-110">**Number**</span><span class="sxs-lookup"><span data-stu-id="26641-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="26641-111">Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamNumber, il membro **Number** contiene il valore del parametro specifico del supporto.</span><span class="sxs-lookup"><span data-stu-id="26641-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="26641-112">Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.</span><span class="sxs-lookup"><span data-stu-id="26641-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="26641-113">Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamNumber, il membro **Number** contiene il valore del parametro specifico del supporto.</span><span class="sxs-lookup"><span data-stu-id="26641-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="26641-114">Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.</span><span class="sxs-lookup"><span data-stu-id="26641-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="26641-115">**Stringa**</span><span class="sxs-lookup"><span data-stu-id="26641-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="26641-116">Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamString, il membro della **stringa** contiene il valore del parametro specifico del supporto.</span><span class="sxs-lookup"><span data-stu-id="26641-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="26641-117">**Length**</span><span class="sxs-lookup"><span data-stu-id="26641-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="26641-118">Specifica la lunghezza, in caratteri, della stringa a cui punta il membro **dati** .</span><span class="sxs-lookup"><span data-stu-id="26641-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="26641-119">**Dati**</span><span class="sxs-lookup"><span data-stu-id="26641-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="26641-120">Puntatore a un buffer che contiene il valore stringa di un parametro specifico del supporto.</span><span class="sxs-lookup"><span data-stu-id="26641-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26641-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26641-121">Requirements</span></span>



| <span data-ttu-id="26641-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26641-122">Requirement</span></span> | <span data-ttu-id="26641-123">Valore</span><span class="sxs-lookup"><span data-stu-id="26641-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26641-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26641-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26641-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26641-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="26641-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26641-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26641-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26641-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="26641-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="26641-128">End of client support</span></span><br/>    | <span data-ttu-id="26641-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26641-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="26641-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="26641-130">End of server support</span></span><br/>    | <span data-ttu-id="26641-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="26641-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="26641-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26641-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="26641-133"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="26641-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26641-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26641-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26641-135">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="26641-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="26641-136">Unione di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="26641-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="26641-137">**\_parametri RAS**</span><span class="sxs-lookup"><span data-stu-id="26641-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="26641-138">**\_formato params \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="26641-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





