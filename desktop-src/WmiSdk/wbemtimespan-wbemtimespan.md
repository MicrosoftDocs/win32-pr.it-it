---
description: Il costruttore della classe WBEMTimeSpan crea un oggetto intervallo di tempo. Il costruttore è sovraccarico.
audience: developer
ms.assetid: 337dc247-9904-457a-a1f3-e1cf29b61126
ms.tgt_platform: multiple
title: 'Costruttori WBEMTimeSpan:: WbemTimeSpan (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: af5724a91ab50b5286e23b3c8095163e415d95e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233981"
---
# <a name="wbemtimespanwbemtimespan-constructors"></a><span data-ttu-id="f552d-104">Costruttori WBEMTimeSpan:: WbemTimeSpan</span><span class="sxs-lookup"><span data-stu-id="f552d-104">WBEMTimeSpan::WbemTimeSpan constructors</span></span>

<span data-ttu-id="f552d-105">\[La classe [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="f552d-105">\[The [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="f552d-106">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="f552d-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="f552d-107">Il costruttore della classe **WBEMTimeSpan** crea un oggetto intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="f552d-107">The **WBEMTimeSpan** class constructor creates a time span object.</span></span> <span data-ttu-id="f552d-108">Il costruttore è sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="f552d-108">The constructor is overloaded.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f552d-109">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="f552d-109">Overload list</span></span>



| <span data-ttu-id="f552d-110">Costruttore</span><span class="sxs-lookup"><span data-stu-id="f552d-110">Constructor</span></span>                                                                                                 | <span data-ttu-id="f552d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f552d-111">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="f552d-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="f552d-112">[**WBEMTimeSpan()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                                      | <span data-ttu-id="f552d-113">Crea un oggetto intervallo di tempo non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="f552d-113">Creates an uninitialized time span object.</span></span><br/>                        |
| <span data-ttu-id="f552d-114">[**WBEMTimeSpan (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="f552d-114">[**WBEMTimeSpan(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>                                               | <span data-ttu-id="f552d-115">Inizializza il nuovo oggetto intervallo di tempo su valore nel parametro.</span><span class="sxs-lookup"><span data-stu-id="f552d-115">Initializes the new time span object to value in the parameter.</span></span><br/>   |
| <span data-ttu-id="f552d-116">[**WBEMTimeSpan (int, int, int, int, int, int, int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span><span class="sxs-lookup"><span data-stu-id="f552d-116">[**WBEMTimeSpan(int,int,int,int,int,int,int)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-wbemtimespan(int_int_int_int_int_int_int))</span></span> | <span data-ttu-id="f552d-117">Inizializza il nuovo oggetto intervallo di tempo sui valori nei parametri.</span><span class="sxs-lookup"><span data-stu-id="f552d-117">Initializes the new time span object to values in the parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f552d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f552d-118">Requirements</span></span>



| <span data-ttu-id="f552d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f552d-119">Requirement</span></span> | <span data-ttu-id="f552d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f552d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f552d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f552d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f552d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f552d-122">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f552d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f552d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f552d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f552d-124">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f552d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f552d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f552d-126"><dt>WbemTime. h</dt></span><span class="sxs-lookup"><span data-stu-id="f552d-126"><dt>WbemTime.h</dt></span></span> </dl>                                                                         |
| <span data-ttu-id="f552d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f552d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f552d-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f552d-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="f552d-129">�</span><span class="sxs-lookup"><span data-stu-id="f552d-129">�</span></span>

<span data-ttu-id="f552d-130">�</span><span class="sxs-lookup"><span data-stu-id="f552d-130">�</span></span>
