---
description: Questa funzione Abilita o Disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978631"
---
# <a name="enableeudc-function"></a><span data-ttu-id="04383-103">EnableEUDC (funzione)</span><span class="sxs-lookup"><span data-stu-id="04383-103">EnableEUDC function</span></span>

<span data-ttu-id="04383-104">Questa funzione Abilita o Disabilita il supporto per i caratteri definiti dall'utente finale (EUDC).</span><span class="sxs-lookup"><span data-stu-id="04383-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="04383-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04383-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="04383-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04383-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04383-107">*fEnableEUDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04383-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04383-108">Valore booleano impostato su **true** per abilitare EUDC e su **false** per disabilitare EUDC.</span><span class="sxs-lookup"><span data-stu-id="04383-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04383-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04383-109">Return value</span></span>

<span data-ttu-id="04383-110">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="04383-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="04383-111">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="04383-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="04383-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="04383-112">Remarks</span></span>

<span data-ttu-id="04383-113">Se EUDC è disabilitato, il tentativo di visualizzare i caratteri EUDC provocherà glifi mancanti o errati.</span><span class="sxs-lookup"><span data-stu-id="04383-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="04383-114">Durante la multisessione, questa funzione influiscono solo sulla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="04383-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="04383-115">Si consiglia di utilizzare questa funzione con Windows XP SP2 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="04383-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="04383-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04383-116">Requirements</span></span>



| <span data-ttu-id="04383-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04383-117">Requirement</span></span> | <span data-ttu-id="04383-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04383-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04383-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04383-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04383-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04383-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="04383-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04383-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04383-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04383-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="04383-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="04383-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="04383-124"><dt>Gdi32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04383-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="04383-125">DLL</span><span class="sxs-lookup"><span data-stu-id="04383-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04383-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04383-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




