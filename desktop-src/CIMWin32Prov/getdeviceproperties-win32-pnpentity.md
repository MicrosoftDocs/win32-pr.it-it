---
description: Ottiene le proprietà specificate del dispositivo Plug and Play.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Metodo GetDeviceProperties della classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049153"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="ee7dd-103">Metodo GetDeviceProperties della \_ classe PnPEntity Win32</span><span class="sxs-lookup"><span data-stu-id="ee7dd-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="ee7dd-104">Ottiene le proprietà specificate del dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee7dd-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="ee7dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee7dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7dd-107">*devicePropertyKeys* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ee7dd-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7dd-108">Proprietà da restituire.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="ee7dd-109">*deviceProperties* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee7dd-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7dd-110">Proprietà richieste nei sottotipi appropriati della classe astratta [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ee7dd-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee7dd-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee7dd-111">Requirements</span></span>



| <span data-ttu-id="ee7dd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee7dd-112">Requirement</span></span> | <span data-ttu-id="ee7dd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ee7dd-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7dd-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee7dd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7dd-115">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ee7dd-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee7dd-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee7dd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7dd-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ee7dd-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="ee7dd-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee7dd-118">Namespace</span></span><br/>                | <span data-ttu-id="ee7dd-119">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ee7dd-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee7dd-120">MOF</span><span class="sxs-lookup"><span data-stu-id="ee7dd-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee7dd-121"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee7dd-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee7dd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ee7dd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee7dd-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee7dd-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee7dd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee7dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7dd-125">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="ee7dd-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




