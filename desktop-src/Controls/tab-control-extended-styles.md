---
title: Stili estesi del controllo Tab (CommCtrl. h)
description: Il controllo struttura a schede supporta ora gli stili estesi. Questi stili vengono modificati usando i messaggi TCM \_ GETEXTENDEDSTYLE e TCM \_ SETEXTENDEDSTYLE e non devono essere confusi con gli stili di finestra estesi passati a CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327599"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="7d7da-104">Stili estesi del controllo Tab</span><span class="sxs-lookup"><span data-stu-id="7d7da-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="7d7da-105">Il controllo struttura a schede supporta ora gli stili estesi.</span><span class="sxs-lookup"><span data-stu-id="7d7da-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="7d7da-106">Questi stili vengono modificati usando i messaggi [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) e [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) e non devono essere confusi con gli stili di finestra estesi passati a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="7d7da-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="7d7da-107">Costante</span><span class="sxs-lookup"><span data-stu-id="7d7da-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="7d7da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d7da-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="7d7da-109"><dt>**TC \_ ex \_ FLATSEPARATORS**</dt></span><span class="sxs-lookup"><span data-stu-id="7d7da-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="7d7da-110">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7d7da-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="7d7da-111">Il controllo struttura a schede trarrà separatori tra le voci di scheda.</span><span class="sxs-lookup"><span data-stu-id="7d7da-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="7d7da-112">Questo stile esteso interessa solo i controlli struttura a schede con i [**\_ pulsanti TCS**](tab-control-styles.md) e gli stili [**\_ FLATBUTTONS di TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7d7da-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="7d7da-113">Per impostazione predefinita, la creazione del controllo struttura a schede con lo stile **\_ FLATBUTTONS di TCS** imposta questo stile esteso.</span><span class="sxs-lookup"><span data-stu-id="7d7da-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="7d7da-114">Se non sono necessari separatori, è necessario rimuovere questo stile esteso dopo aver creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="7d7da-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="7d7da-115"><dt>**TC \_ ex \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="7d7da-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="7d7da-116">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7d7da-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="7d7da-117">Il controllo struttura a schede genera codici di notifica [ \_ GetObject TCN](tcn-getobject.md) per richiedere un oggetto di destinazione di rilascio quando un oggetto viene trascinato sugli elementi di tabulazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="7d7da-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="7d7da-118">Prima di impostare questo stile, l'applicazione deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) .</span><span class="sxs-lookup"><span data-stu-id="7d7da-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="7d7da-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d7da-119">Requirements</span></span>



| <span data-ttu-id="7d7da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d7da-120">Requirement</span></span> | <span data-ttu-id="7d7da-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7d7da-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7da-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d7da-122">Header</span></span><br/> | <dl> <span data-ttu-id="7d7da-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d7da-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

