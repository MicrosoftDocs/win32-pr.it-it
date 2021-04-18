---
description: Il metodo Mid estrae una sottostringa di lunghezza nCount caratteri da una stringa CHString, a partire dalla posizione nFirst (in base zero). Il metodo restituisce una copia della sottostringa estratta.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: 'Metodi CHString:: Mid (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5d05259128f80bcb21d00144d19002ca58ce39c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313688"
---
# <a name="chstringmid-methods"></a><span data-ttu-id="b9cd8-104">Metodi CHString:: Mid</span><span class="sxs-lookup"><span data-stu-id="b9cd8-104">CHString::Mid methods</span></span>

<span data-ttu-id="b9cd8-105">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b9cd8-106">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="b9cd8-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b9cd8-107">Il metodo **Mid** estrae una sottostringa di lunghezza *nCount* caratteri da una stringa [**CHString**](chstring.md) , a partire dalla posizione *nFirst* (in base zero).</span><span class="sxs-lookup"><span data-stu-id="b9cd8-107">The **Mid** method extracts a substring of length *nCount* characters from a [**CHString**](chstring.md) string, starting at position *nFirst* (zero-based).</span></span> <span data-ttu-id="b9cd8-108">Il metodo restituisce una copia della sottostringa estratta.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-108">The method returns a copy of the extracted substring.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b9cd8-109">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="b9cd8-109">Overload list</span></span>



| <span data-ttu-id="b9cd8-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="b9cd8-110">Method</span></span>                                        | <span data-ttu-id="b9cd8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9cd8-111">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| <span data-ttu-id="b9cd8-112">[**Mid (int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span><span class="sxs-lookup"><span data-stu-id="b9cd8-112">[**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int))</span></span> | <span data-ttu-id="b9cd8-113">Estrae una sottostringa di lunghezza e punto iniziale specificati.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-113">Extracts a substring of specified length and beginning point.</span></span><br/> |
| <span data-ttu-id="b9cd8-114">[**Mid (int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="b9cd8-114">[**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>         | <span data-ttu-id="b9cd8-115">Estrae una sottostringa a partire da int.</span><span class="sxs-lookup"><span data-stu-id="b9cd8-115">Extracts a substring beginning at int.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="b9cd8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9cd8-116">Requirements</span></span>



| <span data-ttu-id="b9cd8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9cd8-117">Requirement</span></span> | <span data-ttu-id="b9cd8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9cd8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9cd8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9cd8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9cd8-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9cd8-120">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b9cd8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9cd8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9cd8-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9cd8-122">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b9cd8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9cd8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9cd8-124"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9cd8-124"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b9cd8-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9cd8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9cd8-126"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9cd8-126"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="b9cd8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b9cd8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9cd8-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9cd8-128"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="b9cd8-129">�</span><span class="sxs-lookup"><span data-stu-id="b9cd8-129">�</span></span>

<span data-ttu-id="b9cd8-130">�</span><span class="sxs-lookup"><span data-stu-id="b9cd8-130">�</span></span>
