---
title: Proprietà RdpFileContents di IMsRdpClientShell
description: Specifica o Recupera il contenuto del file di Remote Desktop Protocol (RDP) da avviare da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da un altro portale Web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RdpFileContents
- Servizi Desktop remoto proprietà RdpFileContents, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, proprietà RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301988"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="31fda-106">Proprietà IMsRdpClientShell:: RdpFileContents</span><span class="sxs-lookup"><span data-stu-id="31fda-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="31fda-107">Specifica o Recupera il contenuto del file di Remote Desktop Protocol (RDP) da avviare da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da un altro portale Web.</span><span class="sxs-lookup"><span data-stu-id="31fda-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="31fda-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="31fda-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fda-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31fda-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="31fda-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="31fda-110">Property value</span></span>

<span data-ttu-id="31fda-111">Specifica il contenuto del file RDP da avviare dal portale Web.</span><span class="sxs-lookup"><span data-stu-id="31fda-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fda-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31fda-112">Requirements</span></span>



| <span data-ttu-id="31fda-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fda-113">Requirement</span></span> | <span data-ttu-id="31fda-114">Valore</span><span class="sxs-lookup"><span data-stu-id="31fda-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31fda-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31fda-115">Minimum supported client</span></span><br/> | <span data-ttu-id="31fda-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31fda-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31fda-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31fda-117">Minimum supported server</span></span><br/> | <span data-ttu-id="31fda-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31fda-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31fda-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="31fda-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="31fda-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fda-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31fda-121">DLL</span><span class="sxs-lookup"><span data-stu-id="31fda-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31fda-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31fda-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31fda-123">IID</span><span class="sxs-lookup"><span data-stu-id="31fda-123">IID</span></span><br/>                      | <span data-ttu-id="31fda-124">IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="31fda-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="31fda-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31fda-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fda-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="31fda-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





