---
description: Rappresenta le caratteristiche dei colori CIE (International Commission on illuminazione) di un monitor del computer.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Classe WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346506"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="888db-103">Classe WmiMonitorColorCharacteristics</span><span class="sxs-lookup"><span data-stu-id="888db-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="888db-104">La classe **WmiMonitorColorCharacteristics** rappresenta le caratteristiche dei colori CIE (International Commission on illuminazione) di un monitor del computer.</span><span class="sxs-lookup"><span data-stu-id="888db-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="888db-105">I dati corrispondono ai dati nel blocco delle caratteristiche dei colori della struttura di EDID (video Electronics Standard Association) Enhanced Extended Display Data.</span><span class="sxs-lookup"><span data-stu-id="888db-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="888db-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="888db-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="888db-107">Members</span><span class="sxs-lookup"><span data-stu-id="888db-107">Members</span></span>

<span data-ttu-id="888db-108">La classe **WmiMonitorColorCharacteristics** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="888db-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="888db-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="888db-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="888db-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="888db-110">Properties</span></span>

<span data-ttu-id="888db-111">La classe **WmiMonitorColorCharacteristics** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="888db-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="888db-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="888db-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="888db-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="888db-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="888db-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="888db-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="888db-116">**Blue**</span><span class="sxs-lookup"><span data-stu-id="888db-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-117">Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="888db-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="888db-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="888db-119">Coordinate CIE per il blu, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="888db-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="888db-120">**DefaultWhite**</span><span class="sxs-lookup"><span data-stu-id="888db-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-121">Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="888db-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="888db-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="888db-123">Coordinate CIE bianche predefinite.</span><span class="sxs-lookup"><span data-stu-id="888db-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="888db-124">**Green**</span><span class="sxs-lookup"><span data-stu-id="888db-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-125">Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="888db-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="888db-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="888db-127">Coordinate CIE per il verde, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="888db-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="888db-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="888db-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="888db-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888db-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="888db-131">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="888db-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="888db-132">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="888db-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="888db-133">**Red**</span><span class="sxs-lookup"><span data-stu-id="888db-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888db-134">Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="888db-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="888db-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="888db-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="888db-136">Coordinate CIE per il rosso, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="888db-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="888db-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="888db-137">Remarks</span></span>

<span data-ttu-id="888db-138">I valori della cromaticità e del punto bianco sono espressi come numeri frazionari usando un formato di codifica.</span><span class="sxs-lookup"><span data-stu-id="888db-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="888db-139">Questo formato è accurato per la millesima posizione, con una lunghezza di 10 bit.</span><span class="sxs-lookup"><span data-stu-id="888db-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="888db-140">Il bit più significativo (MSB) rappresenta 2 ^-1 e il bit meno significativo (LSB) rappresenta i coefficienti rispettivamente 2 ^-10.</span><span class="sxs-lookup"><span data-stu-id="888db-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="888db-141">La precisione dei valori archiviati nella struttura E-EDID V1. x deve essere precisa a +/-0,005 del valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="888db-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="888db-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="888db-142">Requirements</span></span>



| <span data-ttu-id="888db-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="888db-143">Requirement</span></span> | <span data-ttu-id="888db-144">Valore</span><span class="sxs-lookup"><span data-stu-id="888db-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="888db-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="888db-145">Minimum supported client</span></span><br/> | <span data-ttu-id="888db-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="888db-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="888db-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="888db-147">Minimum supported server</span></span><br/> | <span data-ttu-id="888db-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="888db-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="888db-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="888db-149">Namespace</span></span><br/>                | <span data-ttu-id="888db-150">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="888db-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="888db-151">MOF</span><span class="sxs-lookup"><span data-stu-id="888db-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="888db-152"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="888db-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="888db-153">DLL</span><span class="sxs-lookup"><span data-stu-id="888db-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="888db-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="888db-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888db-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="888db-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888db-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="888db-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




