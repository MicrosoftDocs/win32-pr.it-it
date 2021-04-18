---
description: Il metodo InsertAt inserisce un elemento (o più copie di un elemento) o tutti gli elementi di un'altra matrice in corrispondenza di un indice specificato.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: 'Metodi CHStringArray:: InsertAt (ChStrArr. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4047b740778c8d0adf1f2b5981b2f3aac5ba9529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318874"
---
# <a name="chstringarrayinsertat-methods"></a><span data-ttu-id="d3864-103">Metodi CHStringArray:: InsertAt</span><span class="sxs-lookup"><span data-stu-id="d3864-103">CHStringArray::InsertAt methods</span></span>

<span data-ttu-id="d3864-104">\[La classe [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie.</span><span class="sxs-lookup"><span data-stu-id="d3864-104">\[The [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d3864-105">Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]</span><span class="sxs-lookup"><span data-stu-id="d3864-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d3864-106">Il metodo **InsertAt** inserisce un elemento (o più copie di un elemento) o tutti gli elementi di un'altra matrice in corrispondenza di un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="d3864-106">The **InsertAt** method inserts an element (or multiple copies of an element) or all the elements of another array at a specified index.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d3864-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="d3864-107">Overload list</span></span>



| <span data-ttu-id="d3864-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="d3864-108">Method</span></span>                                                                               | <span data-ttu-id="d3864-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3864-109">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3864-110">[**InsertAt (int, LPCWSTR, int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3864-110">[**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))</span></span>       | <span data-ttu-id="d3864-111">Inserisce uno o più elementi in corrispondenza di un indice specificato in una matrice.</span><span class="sxs-lookup"><span data-stu-id="d3864-111">Inserts one or more elements at a specified index in an array.</span></span><br/>                                               |
| <span data-ttu-id="d3864-112">[**InsertAt (int, CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="d3864-112">[**InsertAt(int,CHStringArray\*)**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span> | <span data-ttu-id="d3864-113">Inserisce tutti gli elementi di un altro [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) in corrispondenza di un indice specificato in una matrice.</span><span class="sxs-lookup"><span data-stu-id="d3864-113">Inserts all the elements of another [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) at a specified index in an array.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d3864-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3864-114">Requirements</span></span>



| <span data-ttu-id="d3864-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3864-115">Requirement</span></span> | <span data-ttu-id="d3864-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3864-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3864-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3864-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3864-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3864-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d3864-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3864-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3864-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3864-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d3864-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3864-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3864-122"><dt>ChStrArr. h (include FwCommon. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3864-122"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d3864-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3864-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3864-124"><dt>FrameDyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3864-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d3864-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3864-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3864-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3864-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3864-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3864-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3864-128">**CHStringArray**</span><span class="sxs-lookup"><span data-stu-id="d3864-128">**CHStringArray**</span></span>](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

<span data-ttu-id="d3864-129">�</span><span class="sxs-lookup"><span data-stu-id="d3864-129">�</span></span>

<span data-ttu-id="d3864-130">�</span><span class="sxs-lookup"><span data-stu-id="d3864-130">�</span></span>
