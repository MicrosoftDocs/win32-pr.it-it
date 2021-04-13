---
title: WM/Track
description: L'attributo WM/Track contiene il numero di traccia del contenuto. Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti. Il nuovo contenuto deve invece usare l'attributo WM/numero.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Track Windows Media Format
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397163"
---
# <a name="wmtrack"></a><span data-ttu-id="caf21-106">WM/Track</span><span class="sxs-lookup"><span data-stu-id="caf21-106">WM/Track</span></span>

<span data-ttu-id="caf21-107">L'attributo **WM/Track** contiene il numero di traccia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="caf21-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="caf21-108">Questo attributo è in base zero ed è supportato per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="caf21-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="caf21-109">Il nuovo contenuto deve invece usare l'attributo [**WM/numero**](wm-tracknumber.md) .</span><span class="sxs-lookup"><span data-stu-id="caf21-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="caf21-110">Costante globale</span><span class="sxs-lookup"><span data-stu-id="caf21-110">Global Constant</span></span>

<span data-ttu-id="caf21-111">g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="caf21-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="caf21-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="caf21-112">Data Type</span></span>

<span data-ttu-id="caf21-113">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="caf21-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="caf21-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="caf21-114">Remarks</span></span>

<span data-ttu-id="caf21-115">Molte applicazioni esistenti scrivono il valore per **WM/Track** come **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="caf21-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="caf21-116">Se si crea un'applicazione che riproduce file da origini sconosciute, è necessario includere il codice per gestire i valori stringa e **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="caf21-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="caf21-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caf21-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf21-118">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="caf21-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




