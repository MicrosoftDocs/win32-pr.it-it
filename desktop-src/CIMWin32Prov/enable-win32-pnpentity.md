---
description: Abilita questa Plug and Play dispositivo.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Metodo Enable della classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304696"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="eea91-103">Metodo Enable della classe Win32 \_ PnPEntity</span><span class="sxs-lookup"><span data-stu-id="eea91-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="eea91-104">Abilita questa Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eea91-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eea91-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="eea91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eea91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea91-107">*rebootNeeded* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eea91-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eea91-108">Indica se è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="eea91-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eea91-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eea91-109">Requirements</span></span>



| <span data-ttu-id="eea91-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea91-110">Requirement</span></span> | <span data-ttu-id="eea91-111">Valore</span><span class="sxs-lookup"><span data-stu-id="eea91-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea91-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea91-112">Minimum supported client</span></span><br/> | <span data-ttu-id="eea91-113">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="eea91-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eea91-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea91-114">Minimum supported server</span></span><br/> | <span data-ttu-id="eea91-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eea91-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="eea91-116">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eea91-116">Namespace</span></span><br/>                | <span data-ttu-id="eea91-117">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="eea91-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eea91-118">MOF</span><span class="sxs-lookup"><span data-stu-id="eea91-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eea91-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eea91-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eea91-120">DLL</span><span class="sxs-lookup"><span data-stu-id="eea91-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea91-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea91-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea91-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eea91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea91-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="eea91-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




