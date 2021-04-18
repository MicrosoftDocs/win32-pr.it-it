---
description: Il metodo di overload FormatMessageW formatta una stringa di messaggio.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: 'Metodi CHString:: FormatMessageW (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a4f6be83c2cec8f3ae02cdbafac8a6c10ab72578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313198"
---
# <a name="chstringformatmessagew-methods"></a><span data-ttu-id="6b60e-103">Metodi CHString:: FormatMessageW</span><span class="sxs-lookup"><span data-stu-id="6b60e-103">CHString::FormatMessageW methods</span></span>

<span data-ttu-id="6b60e-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="6b60e-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="6b60e-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="6b60e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="6b60e-106">Il metodo di overload **FormatMessageW** formatta una stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="6b60e-106">The overloaded **FormatMessageW** method formats a message string.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6b60e-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="6b60e-107">Overload list</span></span>



| <span data-ttu-id="6b60e-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="6b60e-108">Method</span></span>                                                              | <span data-ttu-id="6b60e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b60e-109">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b60e-110">[**FormatMessageW (UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b60e-110">[**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))</span></span>       | <span data-ttu-id="6b60e-111">Formatta questo messaggio in base all'identificatore di risorsa specificato da **uint**.</span><span class="sxs-lookup"><span data-stu-id="6b60e-111">Formats this message according to the resource identifier specified by the **UINT**.</span></span><br/> |
| <span data-ttu-id="6b60e-112">[**FormatMessageW (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span><span class="sxs-lookup"><span data-stu-id="6b60e-112">[**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---))</span></span> | <span data-ttu-id="6b60e-113">Formatta questa stringa di messaggio in base al formato specificato da **LPCWSTR**.</span><span class="sxs-lookup"><span data-stu-id="6b60e-113">Formats this message string according to the format specified by the **LPCWSTR**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="6b60e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b60e-114">Requirements</span></span>



| <span data-ttu-id="6b60e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b60e-115">Requirement</span></span> | <span data-ttu-id="6b60e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6b60e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b60e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b60e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b60e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b60e-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6b60e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b60e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b60e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b60e-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="6b60e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b60e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b60e-122"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b60e-122"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6b60e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b60e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b60e-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b60e-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="6b60e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6b60e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b60e-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b60e-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="6b60e-127">�</span><span class="sxs-lookup"><span data-stu-id="6b60e-127">�</span></span>

<span data-ttu-id="6b60e-128">�</span><span class="sxs-lookup"><span data-stu-id="6b60e-128">�</span></span>
