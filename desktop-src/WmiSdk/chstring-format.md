---
description: Il metodo format formatta e archivia una serie di caratteri e valori in una stringa CHString.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: 'Metodi CHString:: Format (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7187d2c691c6efb2054d766ae432c55be893cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313196"
---
# <a name="chstringformat-methods"></a><span data-ttu-id="4ad39-103">Metodi CHString:: Format</span><span class="sxs-lookup"><span data-stu-id="4ad39-103">CHString::Format methods</span></span>

<span data-ttu-id="4ad39-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="4ad39-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4ad39-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="4ad39-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4ad39-106">Il metodo **Format** formatta e archivia una serie di caratteri e valori in una stringa [**CHString**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad39-106">The **Format** method formats and stores a series of characters and values in a [**CHString**](chstring.md) string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4ad39-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="4ad39-107">Overload list</span></span>



| <span data-ttu-id="4ad39-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="4ad39-108">Method</span></span>                                              | <span data-ttu-id="4ad39-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad39-109">Description</span></span>                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad39-110">[**Formato (UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ad39-110">[**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))</span></span>       | <span data-ttu-id="4ad39-111">Formatta questo CHString in base all'identificatore di risorsa specificato da **uint**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-111">Formats this CHString according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="4ad39-112">[**Formato (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="4ad39-112">[**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---))</span></span> | <span data-ttu-id="4ad39-113">Formatta questo CHString in base al formato specificato da **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="4ad39-113">Formats this CHString according to the format specified by the **LPCWSTR**.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="4ad39-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ad39-114">Requirements</span></span>



| <span data-ttu-id="4ad39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ad39-115">Requirement</span></span> | <span data-ttu-id="4ad39-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4ad39-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad39-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ad39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad39-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ad39-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4ad39-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ad39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad39-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ad39-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4ad39-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ad39-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ad39-122"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad39-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ad39-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="4ad39-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ad39-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ad39-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4ad39-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad39-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad39-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ad39-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="4ad39-127">�</span><span class="sxs-lookup"><span data-stu-id="4ad39-127">�</span></span>

<span data-ttu-id="4ad39-128">�</span><span class="sxs-lookup"><span data-stu-id="4ad39-128">�</span></span>
