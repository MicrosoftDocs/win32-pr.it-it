---
title: Stili di ingrandimento
description: Questo argomento descrive gli stili usati con il controllo Magnifier.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400641"
---
# <a name="magnifier-styles"></a><span data-ttu-id="d353a-103">Stili di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="d353a-103">Magnifier Styles</span></span>

<span data-ttu-id="d353a-104">Questo argomento descrive gli stili usati con il controllo Magnifier.</span><span class="sxs-lookup"><span data-stu-id="d353a-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="d353a-105">Per creare un controllo Magnifier, usare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) e specificare la classe WC_MAGNIFIER Window, insieme a una combinazione degli stili di ingrandimento seguenti.</span><span class="sxs-lookup"><span data-stu-id="d353a-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="d353a-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="d353a-106">Requirement</span></span> | <span data-ttu-id="d353a-107">Valore</span><span class="sxs-lookup"><span data-stu-id="d353a-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="d353a-108">MS_CLIPAROUNDCURSOR 0x0002L</span><span class="sxs-lookup"><span data-stu-id="d353a-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="d353a-109">Ritaglia l'area della finestra di ingrandimento che racchiude il cursore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d353a-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="d353a-110">Questo stile consente all'utente di visualizzare il contenuto della schermata dietro la finestra di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="d353a-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="d353a-111">MS_INVERTCOLORS 0x0004L</span><span class="sxs-lookup"><span data-stu-id="d353a-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="d353a-112">Visualizza il contenuto della schermata ingrandita utilizzando i colori invertiti.</span><span class="sxs-lookup"><span data-stu-id="d353a-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="d353a-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span><span class="sxs-lookup"><span data-stu-id="d353a-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="d353a-114">Visualizza il cursore di sistema ingrandito insieme al contenuto della schermata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="d353a-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d353a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d353a-115">Requirements</span></span>

| <span data-ttu-id="d353a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d353a-116">Requirement</span></span> | <span data-ttu-id="d353a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d353a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d353a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d353a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d353a-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d353a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d353a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d353a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d353a-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d353a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d353a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d353a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d353a-123"><dt>Ingrandimento. h</dt></span><span class="sxs-lookup"><span data-stu-id="d353a-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d353a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d353a-124">See also</span></span>

[<span data-ttu-id="d353a-125">Costanti</span><span class="sxs-lookup"><span data-stu-id="d353a-125">Constants</span></span>](entry-magapi-constants.md)
