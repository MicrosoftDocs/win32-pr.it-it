---
description: Rappresenta le informazioni di identificazione relative a un monitor video, ad esempio il nome del produttore, l'anno di produzione o il numero di serie.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Classe WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 485b42a86ca67d15ec00be13992c17b31ed51608
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323873"
---
# <a name="wmimonitorid-class"></a><span data-ttu-id="06b0c-103">Classe WmiMonitorID</span><span class="sxs-lookup"><span data-stu-id="06b0c-103">WmiMonitorID class</span></span>

<span data-ttu-id="06b0c-104">La classe WMI **WmiMonitorID** rappresenta le informazioni di identificazione relative a un monitor video, ad esempio il nome del produttore, l'anno di produzione o il numero di serie.</span><span class="sxs-lookup"><span data-stu-id="06b0c-104">The **WmiMonitorID** WMI class represents the identifying information about a video monitor, such as manufacturer name, year of manufacture, or serial number.</span></span> <span data-ttu-id="06b0c-105">I dati in questa classe corrispondono ai dati nel blocco di identificazione del fornitore/prodotto della definizione di input video dello standard EDID (video Electronics Standard Association) avanzato.</span><span class="sxs-lookup"><span data-stu-id="06b0c-105">The data in this class correspond to data in the Vendor/Product Identification block of Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b0c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b0c-106">Syntax</span></span>

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a><span data-ttu-id="06b0c-107">Members</span><span class="sxs-lookup"><span data-stu-id="06b0c-107">Members</span></span>

<span data-ttu-id="06b0c-108">La classe **WmiMonitorID** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06b0c-108">The **WmiMonitorID** class has these types of members:</span></span>

-   [<span data-ttu-id="06b0c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06b0c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06b0c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06b0c-110">Properties</span></span>

<span data-ttu-id="06b0c-111">La classe **WmiMonitorID** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06b0c-111">The **WmiMonitorID** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06b0c-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="06b0c-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="06b0c-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="06b0c-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="06b0c-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06b0c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-119">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="06b0c-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-120">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="06b0c-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-121">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="06b0c-121">**ManufacturerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-122">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-124">Nome del produttore.</span><span class="sxs-lookup"><span data-stu-id="06b0c-124">Name of manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-125">**ManufacturerNameLength**</span><span class="sxs-lookup"><span data-stu-id="06b0c-125">**ManufacturerNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-128">Lunghezza del nome del produttore che si trova nella proprietà **manufacturname** .</span><span class="sxs-lookup"><span data-stu-id="06b0c-128">Length of manufacturer name located in the **ManufacturerName** property.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-129">**ProductCodeID**</span><span class="sxs-lookup"><span data-stu-id="06b0c-129">**ProductCodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-130">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-132">ID del codice prodotto assegnato dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="06b0c-132">Vendor assigned product code ID.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-133">**SerialNumberID**</span><span class="sxs-lookup"><span data-stu-id="06b0c-133">**SerialNumberID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-136">Numero di serie.</span><span class="sxs-lookup"><span data-stu-id="06b0c-136">Serial number.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-137">UserFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06b0c-137">UserFriendlyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-140">Nome descrittivo del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="06b0c-140">The friendly name of the monitor.</span></span> <span data-ttu-id="06b0c-141">Le dimensioni del nome corrispondono alla lunghezza specificata dalla proprietà UserFriendlyNameLength.</span><span class="sxs-lookup"><span data-stu-id="06b0c-141">The size of the name is the length specified by the UserFriendlyNameLength property.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-142">UserFriendlyNameLength</span><span class="sxs-lookup"><span data-stu-id="06b0c-142">UserFriendlyNameLength</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-143">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-145">Numero di caratteri nel nome che si trova nella proprietà UserFriendlyName.</span><span class="sxs-lookup"><span data-stu-id="06b0c-145">Number of characters in the name located in the UserFriendlyName property.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-146">**WeekOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="06b0c-146">**WeekOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-147">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="06b0c-147">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-149">Settimana di produzione per numero di settimana.</span><span class="sxs-lookup"><span data-stu-id="06b0c-149">Week of manufacture by week number.</span></span> <span data-ttu-id="06b0c-150">L'intervallo è compreso tra 1 e 53.</span><span class="sxs-lookup"><span data-stu-id="06b0c-150">The range is from 1 through 53.</span></span> <span data-ttu-id="06b0c-151">Zero (0) non è definito.</span><span class="sxs-lookup"><span data-stu-id="06b0c-151">Zero (0) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="06b0c-152">**YearOfManufacture**</span><span class="sxs-lookup"><span data-stu-id="06b0c-152">**YearOfManufacture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06b0c-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06b0c-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06b0c-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06b0c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06b0c-155">Anno di produzione.</span><span class="sxs-lookup"><span data-stu-id="06b0c-155">Year of manufacture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06b0c-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="06b0c-156">Remarks</span></span>

<span data-ttu-id="06b0c-157">Per una discussione su come tradurre gli array che archiviano gli ID dei numeri di serie, vedere l'articolo relativo alle [informazioni di monitoraggio per Reporting con Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) Blog.</span><span class="sxs-lookup"><span data-stu-id="06b0c-157">For a discussion on how to translate the arrays that store serial number ID's, see the [Reporting Monitor information with Configuration Manager](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog article.</span></span>

## <a name="examples"></a><span data-ttu-id="06b0c-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="06b0c-158">Examples</span></span>

<span data-ttu-id="06b0c-159">Nell'esempio di PowerShell seguente viene recuperato il numero di serie di più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="06b0c-159">The following PowerShell example retrieves the serial number of multiple monitors.</span></span>


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



<span data-ttu-id="06b0c-160">Il codice VBScript seguente recupera anche le informazioni sull'ID di monitoraggio da un sistema.</span><span class="sxs-lookup"><span data-stu-id="06b0c-160">The following VBScript code also retrieves monitor ID information from a system.</span></span>


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a><span data-ttu-id="06b0c-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06b0c-161">Requirements</span></span>



| <span data-ttu-id="06b0c-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b0c-162">Requirement</span></span> | <span data-ttu-id="06b0c-163">Valore</span><span class="sxs-lookup"><span data-stu-id="06b0c-163">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b0c-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b0c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="06b0c-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06b0c-165">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="06b0c-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b0c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="06b0c-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06b0c-167">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="06b0c-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06b0c-168">Namespace</span></span><br/>                | <span data-ttu-id="06b0c-169">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="06b0c-169">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="06b0c-170">MOF</span><span class="sxs-lookup"><span data-stu-id="06b0c-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06b0c-171"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06b0c-171"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="06b0c-172">DLL</span><span class="sxs-lookup"><span data-stu-id="06b0c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b0c-173"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b0c-173"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b0c-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06b0c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b0c-175">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="06b0c-175">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

