---
description: Disabilita questo dispositivo Plug and Play.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Metodo Disable della classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523394"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="9cac2-103">Metodo Disable della classe Win32 \_ PnPEntity</span><span class="sxs-lookup"><span data-stu-id="9cac2-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="9cac2-104">Disabilita questo dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="9cac2-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cac2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cac2-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="9cac2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cac2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cac2-107">*rebootNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9cac2-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cac2-108">Indica se è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9cac2-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9cac2-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cac2-109">Requirements</span></span>



| <span data-ttu-id="9cac2-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cac2-110">Requirement</span></span> | <span data-ttu-id="9cac2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="9cac2-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cac2-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cac2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9cac2-113">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9cac2-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9cac2-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cac2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9cac2-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9cac2-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="9cac2-116">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cac2-116">Namespace</span></span><br/>                | <span data-ttu-id="9cac2-117">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9cac2-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cac2-118">MOF</span><span class="sxs-lookup"><span data-stu-id="9cac2-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cac2-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cac2-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cac2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9cac2-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cac2-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cac2-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cac2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cac2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cac2-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="9cac2-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




