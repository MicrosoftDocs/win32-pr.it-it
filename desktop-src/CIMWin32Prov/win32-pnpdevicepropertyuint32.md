---
description: Rappresenta una proprietà del dispositivo PnP di tipo UInt32.
ms.assetid: 5348DBFC-67AD-4A07-A054-F713B3AB468D
ms.tgt_platform: multiple
title: Classe Win32_PnPDevicePropertyUint32
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevicePropertyUint32
- Win32_PnPDevicePropertyUint32.Key
- Win32_PnPDevicePropertyUint32.KeyName
- Win32_PnPDevicePropertyUint32.Type
- Win32_PnPDevicePropertyUint32.DeviceID
- Win32_PnPDevicePropertyUint32.Data
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3805ebb3f0c11f94138da6c38b4dfe058f98464
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127686"
---
# <a name="win32_pnpdevicepropertyuint32-class"></a><span data-ttu-id="1356e-103">Win32 \_ PnPDevicePropertyUint32 (classe)</span><span class="sxs-lookup"><span data-stu-id="1356e-103">Win32\_PnPDevicePropertyUint32 class</span></span>

<span data-ttu-id="1356e-104">Rappresenta una proprietà del dispositivo PnP di tipo **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="1356e-104">Represents a PnP device property of type **Uint32**.</span></span>

<span data-ttu-id="1356e-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1356e-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1356e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1356e-106">Syntax</span></span>

``` syntax
class Win32_PnPDevicePropertyUint32 : Win32_PnPDeviceProperty
{
  string Key;
  string KeyName;
  Uint32 Type;
  string DeviceID;
  Uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="1356e-107">Members</span><span class="sxs-lookup"><span data-stu-id="1356e-107">Members</span></span>

<span data-ttu-id="1356e-108">La classe **Win32 \_ PnPDevicePropertyUint32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1356e-108">The **Win32\_PnPDevicePropertyUint32** class has these types of members:</span></span>

-   [<span data-ttu-id="1356e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1356e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1356e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1356e-110">Properties</span></span>

<span data-ttu-id="1356e-111">La classe **Win32 \_ PnPDevicePropertyUint32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1356e-111">The **Win32\_PnPDevicePropertyUint32** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1356e-112">**Dati**</span><span class="sxs-lookup"><span data-stu-id="1356e-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1356e-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1356e-113">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1356e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1356e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1356e-115">Valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1356e-115">The property value.</span></span>

</dd> <dt>

<span data-ttu-id="1356e-116">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1356e-116">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1356e-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1356e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1356e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1356e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1356e-119">Identifica il dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="1356e-119">Identifies the PnP device.</span></span>

<span data-ttu-id="1356e-120">Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1356e-120">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="1356e-121">**Chiave**</span><span class="sxs-lookup"><span data-stu-id="1356e-121">**Key**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1356e-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1356e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1356e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1356e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1356e-124">Valore della coppia chiave Name-Value che identifica la proprietà **dei dati** .</span><span class="sxs-lookup"><span data-stu-id="1356e-124">The value of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="1356e-125">Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1356e-125">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="1356e-126">**KeyName**</span><span class="sxs-lookup"><span data-stu-id="1356e-126">**KeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1356e-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1356e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1356e-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1356e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1356e-129">Nome della coppia di Name-Value chiave che identifica la proprietà **dei dati** .</span><span class="sxs-lookup"><span data-stu-id="1356e-129">The name of the Key Name-Value pair that identifies the **Data** property.</span></span>

<span data-ttu-id="1356e-130">Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1356e-130">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

</dd> <dt>

<span data-ttu-id="1356e-131">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1356e-131">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1356e-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1356e-132">Data type: **Uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1356e-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1356e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1356e-134">Tipo della proprietà dei **dati** .</span><span class="sxs-lookup"><span data-stu-id="1356e-134">The type of the **Data** property.</span></span>

<span data-ttu-id="1356e-135">Questa proprietà viene ereditata da [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1356e-135">This property is inherited from [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md).</span></span>

<span data-ttu-id="1356e-136">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="1356e-136">The possible values are.</span></span>

<dt>

<span id="Empty"></span><span id="empty"></span><span id="EMPTY"></span>

<span data-ttu-id="1356e-137">**Empty** (0)</span><span class="sxs-lookup"><span data-stu-id="1356e-137">**Empty** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Null"></span><span id="null"></span><span id="NULL"></span>

<span data-ttu-id="1356e-138">**Null** (1)</span><span class="sxs-lookup"><span data-stu-id="1356e-138">**Null** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SByte"></span><span id="sbyte"></span><span id="SBYTE"></span>

<span data-ttu-id="1356e-139">**SByte** (2)</span><span class="sxs-lookup"><span data-stu-id="1356e-139">**SByte** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Byte"></span><span id="byte"></span><span id="BYTE"></span>

<span data-ttu-id="1356e-140">**Byte** (3)</span><span class="sxs-lookup"><span data-stu-id="1356e-140">**Byte** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16"></span><span id="int16"></span><span id="INT16"></span>

<span data-ttu-id="1356e-141">**Int16** (4)</span><span class="sxs-lookup"><span data-stu-id="1356e-141">**Int16** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16"></span><span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="1356e-142">**UInt16** (5)</span><span class="sxs-lookup"><span data-stu-id="1356e-142">**UInt16** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Int32"></span><span id="int32"></span><span id="INT32"></span>

<span data-ttu-id="1356e-143">**Int32** (6)</span><span class="sxs-lookup"><span data-stu-id="1356e-143">**Int32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Uint32"></span><span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="1356e-144">**UInt32** (7)</span><span class="sxs-lookup"><span data-stu-id="1356e-144">**Uint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64"></span><span id="int64"></span><span id="INT64"></span>

<span data-ttu-id="1356e-145">**Int64** (8)</span><span class="sxs-lookup"><span data-stu-id="1356e-145">**Int64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64"></span><span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="1356e-146">**UInt64** (9)</span><span class="sxs-lookup"><span data-stu-id="1356e-146">**UInt64** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Float"></span><span id="float"></span><span id="FLOAT"></span>

<span data-ttu-id="1356e-147">**Float** (10)</span><span class="sxs-lookup"><span data-stu-id="1356e-147">**Float** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Double"></span><span id="double"></span><span id="DOUBLE"></span>

<span data-ttu-id="1356e-148">**Double** (11)</span><span class="sxs-lookup"><span data-stu-id="1356e-148">**Double** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Decimal"></span><span id="decimal"></span><span id="DECIMAL"></span>

<span data-ttu-id="1356e-149">**Decimale** (12)</span><span class="sxs-lookup"><span data-stu-id="1356e-149">**Decimal** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Guid"></span><span id="guid"></span><span id="GUID"></span>

<span data-ttu-id="1356e-150">**GUID** (13)</span><span class="sxs-lookup"><span data-stu-id="1356e-150">**Guid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Currency"></span><span id="currency"></span><span id="CURRENCY"></span>

<span data-ttu-id="1356e-151">**Valuta** (14)</span><span class="sxs-lookup"><span data-stu-id="1356e-151">**Currency** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Date"></span><span id="date"></span><span id="DATE"></span>

<span data-ttu-id="1356e-152">**Data** (15)</span><span class="sxs-lookup"><span data-stu-id="1356e-152">**Date** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTime"></span><span id="filetime"></span><span id="FILETIME"></span>

<span data-ttu-id="1356e-153">**FILETIME** (16)</span><span class="sxs-lookup"><span data-stu-id="1356e-153">**FileTime** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="1356e-154">**Valore booleano** (17)</span><span class="sxs-lookup"><span data-stu-id="1356e-154">**Boolean** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="String"></span><span id="string"></span><span id="STRING"></span>

<span data-ttu-id="1356e-155">**Stringa** (18)</span><span class="sxs-lookup"><span data-stu-id="1356e-155">**String** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptor"></span><span id="securitydescriptor"></span><span id="SECURITYDESCRIPTOR"></span>

<span data-ttu-id="1356e-156">**SecurityDescriptor** (19)</span><span class="sxs-lookup"><span data-stu-id="1356e-156">**SecurityDescriptor** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorString"></span><span id="securitydescriptorstring"></span><span id="SECURITYDESCRIPTORSTRING"></span>

<span data-ttu-id="1356e-157">**SecurityDescriptorString** (20)</span><span class="sxs-lookup"><span data-stu-id="1356e-157">**SecurityDescriptorString** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEY"></span><span id="devpropkey"></span>

<span data-ttu-id="1356e-158">**DEVPROPKEY** (21)</span><span class="sxs-lookup"><span data-stu-id="1356e-158">**DEVPROPKEY** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPE"></span><span id="devproptype"></span>

<span data-ttu-id="1356e-159">**DEVPROPTYPE** (22)</span><span class="sxs-lookup"><span data-stu-id="1356e-159">**DEVPROPTYPE** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1356e-160">**Errore** (23)</span><span class="sxs-lookup"><span data-stu-id="1356e-160">**Error** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatus"></span><span id="ntstatus"></span><span id="NTSTATUS"></span>

<span data-ttu-id="1356e-161">**NTSTATUS** (24)</span><span class="sxs-lookup"><span data-stu-id="1356e-161">**NTStatus** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirect"></span><span id="stringindirect"></span><span id="STRINGINDIRECT"></span>

<span data-ttu-id="1356e-162">**StringIndirect** (25)</span><span class="sxs-lookup"><span data-stu-id="1356e-162">**StringIndirect** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1356e-163">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1356e-163">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="1356e-164">26 – 4097</span><span class="sxs-lookup"><span data-stu-id="1356e-164">26–4097</span></span></dd> <dt>

<span id="SByteArray"></span><span id="sbytearray"></span><span id="SBYTEARRAY"></span>

<span data-ttu-id="1356e-165">**SByteArray** (4098)</span><span class="sxs-lookup"><span data-stu-id="1356e-165">**SByteArray** (4098)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="1356e-166">**Binario** (4099)</span><span class="sxs-lookup"><span data-stu-id="1356e-166">**Binary** (4099)</span></span>


</dt> <dd></dd> <dt>

<span id="Int16Array"></span><span id="int16array"></span><span id="INT16ARRAY"></span>

<span data-ttu-id="1356e-167">**Int16Array** (4100)</span><span class="sxs-lookup"><span data-stu-id="1356e-167">**Int16Array** (4100)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt16Array"></span><span id="uint16array"></span><span id="UINT16ARRAY"></span>

<span data-ttu-id="1356e-168">**Uint16Array** (4101)</span><span class="sxs-lookup"><span data-stu-id="1356e-168">**UInt16Array** (4101)</span></span>


</dt> <dd></dd> <dt>

<span id="Int64Array"></span><span id="int64array"></span><span id="INT64ARRAY"></span>

<span data-ttu-id="1356e-169">**Int64Array** (4102)</span><span class="sxs-lookup"><span data-stu-id="1356e-169">**Int64Array** (4102)</span></span>


</dt> <dd></dd> <dt>

<span id="UInt64Array"></span><span id="uint64array"></span><span id="UINT64ARRAY"></span>

<span data-ttu-id="1356e-170">**UInt64Array** (4103)</span><span class="sxs-lookup"><span data-stu-id="1356e-170">**UInt64Array** (4103)</span></span>


</dt> <dd></dd> <dt>

<span id="FloatArray"></span><span id="floatarray"></span><span id="FLOATARRAY"></span>

<span data-ttu-id="1356e-171">**FloatArray** (4104)</span><span class="sxs-lookup"><span data-stu-id="1356e-171">**FloatArray** (4104)</span></span>


</dt> <dd></dd> <dt>

<span id="DoubleArray"></span><span id="doublearray"></span><span id="DOUBLEARRAY"></span>

<span data-ttu-id="1356e-172">**DoubleArray** (4105)</span><span class="sxs-lookup"><span data-stu-id="1356e-172">**DoubleArray** (4105)</span></span>


</dt> <dd></dd> <dt>

<span id="DecimalArray"></span><span id="decimalarray"></span><span id="DECIMALARRAY"></span>

<span data-ttu-id="1356e-173">**DecimalArray** (4106)</span><span class="sxs-lookup"><span data-stu-id="1356e-173">**DecimalArray** (4106)</span></span>


</dt> <dd></dd> <dt>

<span id="GuidArray"></span><span id="guidarray"></span><span id="GUIDARRAY"></span>

<span data-ttu-id="1356e-174">**GuidArray** (4107)</span><span class="sxs-lookup"><span data-stu-id="1356e-174">**GuidArray** (4107)</span></span>


</dt> <dd></dd> <dt>

<span id="CurrencyArray"></span><span id="currencyarray"></span><span id="CURRENCYARRAY"></span>

<span data-ttu-id="1356e-175">**CurrencyArray** (4108)</span><span class="sxs-lookup"><span data-stu-id="1356e-175">**CurrencyArray** (4108)</span></span>


</dt> <dd></dd> <dt>

<span id="DateArray"></span><span id="datearray"></span><span id="DATEARRAY"></span>

<span data-ttu-id="1356e-176">**DateArray** (4109)</span><span class="sxs-lookup"><span data-stu-id="1356e-176">**DateArray** (4109)</span></span>


</dt> <dd></dd> <dt>

<span id="FileTimeArray"></span><span id="filetimearray"></span><span id="FILETIMEARRAY"></span>

<span data-ttu-id="1356e-177">**FileTimeArray** (4110)</span><span class="sxs-lookup"><span data-stu-id="1356e-177">**FileTimeArray** (4110)</span></span>


</dt> <dd></dd> <dt>

<span id="BooleanArray"></span><span id="booleanarray"></span><span id="BOOLEANARRAY"></span>

<span data-ttu-id="1356e-178">**BooleanArray** (4111)</span><span class="sxs-lookup"><span data-stu-id="1356e-178">**BooleanArray** (4111)</span></span>


</dt> <dd></dd> <dt>

<span id="StringList"></span><span id="stringlist"></span><span id="STRINGLIST"></span>

<span data-ttu-id="1356e-179">**String** (4112)</span><span class="sxs-lookup"><span data-stu-id="1356e-179">**StringList** (4112)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorList"></span><span id="securitydescriptorlist"></span><span id="SECURITYDESCRIPTORLIST"></span>

<span data-ttu-id="1356e-180">**SecurityDescriptorList** (4113)</span><span class="sxs-lookup"><span data-stu-id="1356e-180">**SecurityDescriptorList** (4113)</span></span>


</dt> <dd></dd> <dt>

<span id="SecurityDescriptorStringList"></span><span id="securitydescriptorstringlist"></span><span id="SECURITYDESCRIPTORSTRINGLIST"></span>

<span data-ttu-id="1356e-181">**SecurityDescriptorStringList** (8210)</span><span class="sxs-lookup"><span data-stu-id="1356e-181">**SecurityDescriptorStringList** (8210)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPKEYArray"></span><span id="devpropkeyarray"></span><span id="DEVPROPKEYARRAY"></span>

<span data-ttu-id="1356e-182">**DEVPROPKEYArray** (8211)</span><span class="sxs-lookup"><span data-stu-id="1356e-182">**DEVPROPKEYArray** (8211)</span></span>


</dt> <dd></dd> <dt>

<span id="DEVPROPTYPEArray"></span><span id="devproptypearray"></span><span id="DEVPROPTYPEARRAY"></span>

<span data-ttu-id="1356e-183">**DEVPROPTYPEArray** (8212)</span><span class="sxs-lookup"><span data-stu-id="1356e-183">**DEVPROPTYPEArray** (8212)</span></span>


</dt> <dd></dd> <dt>

<span id="ErrorArray"></span><span id="errorarray"></span><span id="ERRORARRAY"></span>

<span data-ttu-id="1356e-184">**ErrorArray** (4117)</span><span class="sxs-lookup"><span data-stu-id="1356e-184">**ErrorArray** (4117)</span></span>


</dt> <dd></dd> <dt>

<span id="NTStatusArray"></span><span id="ntstatusarray"></span><span id="NTSTATUSARRAY"></span>

<span data-ttu-id="1356e-185">**NTStatusArray** (4118)</span><span class="sxs-lookup"><span data-stu-id="1356e-185">**NTStatusArray** (4118)</span></span>


</dt> <dd></dd> <dt>

<span id="StringIndirectList"></span><span id="stringindirectlist"></span><span id="STRINGINDIRECTLIST"></span>

<span data-ttu-id="1356e-186">**StringIndirectList** (4119)</span><span class="sxs-lookup"><span data-stu-id="1356e-186">**StringIndirectList** (4119)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_-_check_in_devpropdef.h"></span><span id="unknown_-_check_in_devpropdef.h"></span><span id="UNKNOWN_-_CHECK_IN_DEVPROPDEF.H"></span>

<span data-ttu-id="1356e-187">**Unknown-check in devpropdef. h** (4120)</span><span class="sxs-lookup"><span data-stu-id="1356e-187">**Unknown - check in devpropdef.h** (4120)</span></span>


</dt> <dd></dd> <dt>

<span id="TBD"></span><span id="tbd"></span>

<span data-ttu-id="1356e-188">Da **definire (8217** )</span><span class="sxs-lookup"><span data-stu-id="1356e-188">**TBD** (8217)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1356e-189">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1356e-189">**Reserved**</span></span>


</dt> <dd><span data-ttu-id="1356e-190">8218-4294967295</span><span class="sxs-lookup"><span data-stu-id="1356e-190">8218–4294967295</span></span></dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1356e-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1356e-191">Requirements</span></span>



| <span data-ttu-id="1356e-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="1356e-192">Requirement</span></span> | <span data-ttu-id="1356e-193">Valore</span><span class="sxs-lookup"><span data-stu-id="1356e-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1356e-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1356e-194">Minimum supported client</span></span><br/> | <span data-ttu-id="1356e-195">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1356e-195">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1356e-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1356e-196">Minimum supported server</span></span><br/> | <span data-ttu-id="1356e-197">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1356e-197">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="1356e-198">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1356e-198">Namespace</span></span><br/>                | <span data-ttu-id="1356e-199">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1356e-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1356e-200">MOF</span><span class="sxs-lookup"><span data-stu-id="1356e-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1356e-201"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1356e-201"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1356e-202">DLL</span><span class="sxs-lookup"><span data-stu-id="1356e-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1356e-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1356e-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1356e-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1356e-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1356e-205">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="1356e-205">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1356e-206">**\_PnPDeviceProperty Win32**</span><span class="sxs-lookup"><span data-stu-id="1356e-206">**Win32\_PnPDeviceProperty**</span></span>](win32-pnpdeviceproperty.md)
</dt> <dt>

[<span data-ttu-id="1356e-207">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="1356e-207">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md)
</dt> </dl>

 

 




