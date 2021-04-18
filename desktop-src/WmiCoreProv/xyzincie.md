---
description: Contiene le coordinate dello schermo nello spazio dei colori di International Commission on illuminazione (CIE) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Classe XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316997"
---
# <a name="xyzincie-class"></a><span data-ttu-id="cfe12-103">Classe XYZinCIE</span><span class="sxs-lookup"><span data-stu-id="cfe12-103">XYZinCIE class</span></span>

<span data-ttu-id="cfe12-104">La classe WMI **XYZinCIE** contiene le coordinate dello schermo nello spazio dei colori di International Commission on illuminazione (CIE) XYZ.</span><span class="sxs-lookup"><span data-stu-id="cfe12-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe12-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfe12-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="cfe12-106">Members</span><span class="sxs-lookup"><span data-stu-id="cfe12-106">Members</span></span>

<span data-ttu-id="cfe12-107">La classe **XYZinCIE** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cfe12-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="cfe12-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cfe12-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfe12-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cfe12-109">Properties</span></span>

<span data-ttu-id="cfe12-110">La classe **XYZinCIE** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cfe12-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfe12-111">**X**</span><span class="sxs-lookup"><span data-stu-id="cfe12-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfe12-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfe12-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfe12-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cfe12-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfe12-114">Coordinata X.</span><span class="sxs-lookup"><span data-stu-id="cfe12-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="cfe12-115">**S**</span><span class="sxs-lookup"><span data-stu-id="cfe12-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfe12-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfe12-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfe12-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cfe12-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfe12-118">Coordinata Y.</span><span class="sxs-lookup"><span data-stu-id="cfe12-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfe12-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfe12-119">Remarks</span></span>

<span data-ttu-id="cfe12-120">La classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene istanze incorporate della classe **XYZinCIE** per descrivere le caratteristiche dei colori di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cfe12-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="cfe12-121">Per calcolare la coordinata z, in base ai valori x e y, usare la relazione \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="cfe12-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe12-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfe12-122">Requirements</span></span>



| <span data-ttu-id="cfe12-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe12-123">Requirement</span></span> | <span data-ttu-id="cfe12-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe12-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe12-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfe12-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe12-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfe12-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cfe12-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfe12-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe12-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfe12-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cfe12-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cfe12-129">Namespace</span></span><br/>                | <span data-ttu-id="cfe12-130">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="cfe12-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cfe12-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cfe12-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfe12-132"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfe12-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfe12-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cfe12-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfe12-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe12-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe12-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfe12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe12-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="cfe12-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




