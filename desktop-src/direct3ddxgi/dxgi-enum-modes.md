---
description: Opzioni per l'enumerazione delle modalità di visualizzazione.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322524"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="776b1-103">\_modalità di enumerazione DXGI \_</span><span class="sxs-lookup"><span data-stu-id="776b1-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="776b1-104">Opzioni per l'enumerazione delle modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="776b1-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="776b1-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="776b1-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="776b1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="776b1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="776b1-107"><dt>**DXGI \_ Modalità di enumerazione 1UL \_ \_ interlacciato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="776b1-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="776b1-108">Includere le modalità interlacciate.</span><span class="sxs-lookup"><span data-stu-id="776b1-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="776b1-109"><dt>**DXGI \_ Modalità di enumerazione con \_ \_ scalabilità**</dt> <dt>2UL</dt></span><span class="sxs-lookup"><span data-stu-id="776b1-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="776b1-110">Includere le modalità di scalabilità estesa.</span><span class="sxs-lookup"><span data-stu-id="776b1-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="776b1-111"><dt>**DXGI \_ Modalità di enumerazione \_ \_ stereo**</dt> <dt>4UL</dt></span><span class="sxs-lookup"><span data-stu-id="776b1-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="776b1-112">Includere le modalità stereo.</span><span class="sxs-lookup"><span data-stu-id="776b1-112">Include stereo modes.</span></span><br/> <span data-ttu-id="776b1-113">**Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="776b1-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="776b1-114"><dt>**DXGI \_ \_Modalità enum \_ disabilitate 8UL \_ stereo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="776b1-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="776b1-115">Includere le modalità stereo nascoste perché l'utente ha disattivato lo stereo.</span><span class="sxs-lookup"><span data-stu-id="776b1-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="776b1-116">Le applicazioni del pannello di controllo possono usare questa opzione per mostrare le funzionalità stereo che sono state disabilitate come parte di un'interfaccia utente che Abilita e Disabilita lo stereo.</span><span class="sxs-lookup"><span data-stu-id="776b1-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="776b1-117">**Direct3D 11:** Questo valore di enumerazione è supportato a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="776b1-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="776b1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="776b1-118">Remarks</span></span>

<span data-ttu-id="776b1-119">Queste opzioni dei flag vengono usate in [**IDXGIOutput:: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) per enumerare le modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="776b1-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="776b1-120">Queste opzioni dei flag vengono usate anche in [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) per enumerare le modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="776b1-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="776b1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="776b1-121">Requirements</span></span>



| <span data-ttu-id="776b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="776b1-122">Requirement</span></span> | <span data-ttu-id="776b1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="776b1-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="776b1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="776b1-124">Header</span></span><br/> | <dl> <span data-ttu-id="776b1-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="776b1-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776b1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="776b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776b1-127">Costanti DXGI</span><span class="sxs-lookup"><span data-stu-id="776b1-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




