---
title: Struttura WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: La \_ struttura WMDRMNET Policy \_ TRANSCRYPTPLAY include le informazioni sui criteri per la riproduzione di contenuto con Windows Media DRM per i dispositivi di rete.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY_TRANSCRYPTPLAY
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324815"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="ae373-105">\_Struttura TRANSCRYPTPLAY del criterio WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="ae373-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="ae373-106">La struttura **WMDRMNET \_ policy \_ TRANSCRYPTPLAY** include le informazioni sui criteri per la riproduzione di contenuto con Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="ae373-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae373-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae373-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="ae373-108">Members</span><span class="sxs-lookup"><span data-stu-id="ae373-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae373-109">**Globals**</span><span class="sxs-lookup"><span data-stu-id="ae373-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="ae373-110">Struttura dei criteri globali.</span><span class="sxs-lookup"><span data-stu-id="ae373-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="ae373-111">**playOPLs**</span><span class="sxs-lookup"><span data-stu-id="ae373-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="ae373-112">Livelli di protezione dell'output per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ae373-112">Output protection levels for playback.</span></span> <span data-ttu-id="ae373-113">**WMDRMNET \_ POLICY \_ Play \_ OPL** è un tipo definito come [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).</span><span class="sxs-lookup"><span data-stu-id="ae373-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae373-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae373-114">Remarks</span></span>

<span data-ttu-id="ae373-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ae373-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae373-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae373-116">Requirements</span></span>



| <span data-ttu-id="ae373-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae373-117">Requirement</span></span> | <span data-ttu-id="ae373-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ae373-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae373-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae373-119">Header</span></span><br/> | <dl> <span data-ttu-id="ae373-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae373-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae373-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae373-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae373-122">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="ae373-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="ae373-123">**criteri di WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="ae373-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





