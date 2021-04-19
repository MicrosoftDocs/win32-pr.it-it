---
description: Determina se una stringa di applicazione e argomento (&\# 0034; AppName \| topicname&\# 0034;) Usa la sintassi corretta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Funzione NDdeIsValidAppTopicList (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317316"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="0d4b0-103">NDdeIsValidAppTopicList (funzione)</span><span class="sxs-lookup"><span data-stu-id="0d4b0-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="0d4b0-104">\[Il DDE di rete non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="0d4b0-105">Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="0d4b0-106">Determina se un'applicazione e una stringa di argomento ("*appname* \| *topicName*") utilizzano la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d4b0-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="0d4b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d4b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4b0-109">*targetTopic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4b0-110">Puntatore alla stringa dell'applicazione e dell'argomento da convalidare.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="0d4b0-111">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4b0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d4b0-112">Return value</span></span>

<span data-ttu-id="0d4b0-113">Se il parametro *targetTopic* ha una sintassi valida, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="0d4b0-114">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4b0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d4b0-115">Remarks</span></span>

<span data-ttu-id="0d4b0-116">Questa funzione viene chiamata anche da [**NDDEShareAdd**](nddeshareadd.md) quando crea la condivisione DDE.</span><span class="sxs-lookup"><span data-stu-id="0d4b0-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4b0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d4b0-117">Requirements</span></span>



| <span data-ttu-id="0d4b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4b0-118">Requirement</span></span> | <span data-ttu-id="0d4b0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4b0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4b0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4b0-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d4b0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4b0-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d4b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0d4b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d4b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4b0-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b0-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d4b0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d4b0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d4b0-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b0-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="0d4b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0d4b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d4b0-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d4b0-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0d4b0-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0d4b0-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0d4b0-131">**NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0d4b0-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d4b0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d4b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4b0-133">Panoramica di Dynamic Data Exchange di rete</span><span class="sxs-lookup"><span data-stu-id="0d4b0-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="0d4b0-134">Funzioni DDE di rete</span><span class="sxs-lookup"><span data-stu-id="0d4b0-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="0d4b0-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="0d4b0-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




