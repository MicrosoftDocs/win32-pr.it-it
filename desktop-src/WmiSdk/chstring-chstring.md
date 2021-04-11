---
description: Ognuno dei costruttori seguenti Inizializza un nuovo oggetto CHString con i dati specificati.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Costruttori CHString:: CHString (ChString. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231824"
---
# <a name="chstringchstring-constructors"></a><span data-ttu-id="baceb-103">Costruttori CHString:: CHString</span><span class="sxs-lookup"><span data-stu-id="baceb-103">CHString::CHString constructors</span></span>

<span data-ttu-id="baceb-104">\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="baceb-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="baceb-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="baceb-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="baceb-106">Ognuno dei costruttori seguenti Inizializza un nuovo oggetto [**CHString**](chstring.md) con i dati specificati.</span><span class="sxs-lookup"><span data-stu-id="baceb-106">Each of the following constructors initializes a new [**CHString**](chstring.md) object with the specified data.</span></span>

### <a name="overload-list"></a><span data-ttu-id="baceb-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="baceb-107">Overload list</span></span>



| <span data-ttu-id="baceb-108">Costruttore</span><span class="sxs-lookup"><span data-stu-id="baceb-108">Constructor</span></span>                                                                        | <span data-ttu-id="baceb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baceb-109">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="baceb-110">**CHString()**</span><span class="sxs-lookup"><span data-stu-id="baceb-110">**CHString()**</span></span>](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | <span data-ttu-id="baceb-111">Crea un oggetto CHString vuoto.</span><span class="sxs-lookup"><span data-stu-id="baceb-111">Creates an empty CHString object.</span></span><br/>                 |
| <span data-ttu-id="baceb-112">[**CHString (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span><span class="sxs-lookup"><span data-stu-id="baceb-112">[**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))</span></span>                              | <span data-ttu-id="baceb-113">Inizializza con il valore LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="baceb-113">Initializes with the LPCSTR value.</span></span><br/>                |
| <span data-ttu-id="baceb-114">[**CHString (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="baceb-114">[**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))</span></span>                            | <span data-ttu-id="baceb-115">Inizializza con il valore LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="baceb-115">Initializes with the LPCWSTR value.</span></span><br/>               |
| <span data-ttu-id="baceb-116">[**CHString (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span><span class="sxs-lookup"><span data-stu-id="baceb-116">[**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))</span></span>                        | <span data-ttu-id="baceb-117">Inizializza con copie int del valore WCHAR.</span><span class="sxs-lookup"><span data-stu-id="baceb-117">Initializes with int copies of the WCHAR value.</span></span><br/>   |
| <span data-ttu-id="baceb-118">[**CHString (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span><span class="sxs-lookup"><span data-stu-id="baceb-118">[**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))</span></span>                    | <span data-ttu-id="baceb-119">Inizializza con copie int del valore LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="baceb-119">Initializes with int copies of the LPCWSTR value.</span></span><br/> |
| <span data-ttu-id="baceb-120">[**CHString (const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="baceb-120">[**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))</span></span>            | <span data-ttu-id="baceb-121">Replica il parametro CHString.</span><span class="sxs-lookup"><span data-stu-id="baceb-121">Replicates the CHString parameter.</span></span><br/>                |
| <span data-ttu-id="baceb-122">[**CHString (const unsigned char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span><span class="sxs-lookup"><span data-stu-id="baceb-122">[**CHString(const unsigned char\*)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar))</span></span> | <span data-ttu-id="baceb-123">Inizializza con il valore a cui punta char \* .</span><span class="sxs-lookup"><span data-stu-id="baceb-123">Initializes with the value pointed to by char\*.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="baceb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baceb-124">Requirements</span></span>



| <span data-ttu-id="baceb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="baceb-125">Requirement</span></span> | <span data-ttu-id="baceb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="baceb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baceb-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baceb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="baceb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baceb-128">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="baceb-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baceb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="baceb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baceb-130">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="baceb-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baceb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="baceb-132"><dt>ChString. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baceb-132"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="baceb-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="baceb-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="baceb-134"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="baceb-134"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="baceb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="baceb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baceb-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baceb-136"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



<span data-ttu-id="baceb-137">�</span><span class="sxs-lookup"><span data-stu-id="baceb-137">�</span></span>

<span data-ttu-id="baceb-138">�</span><span class="sxs-lookup"><span data-stu-id="baceb-138">�</span></span>
