---
description: Win32 \_ PageFileSetting&\# 8194; Classe WMI che rappresenta le impostazioni di un file di paging.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Classe Win32_PageFileSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305155"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="68e47-103">Win32 \_ PageFileSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="68e47-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="68e47-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileSetting Win32** rappresenta le impostazioni di un file di paging.</span><span class="sxs-lookup"><span data-stu-id="68e47-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="68e47-105">Le informazioni contenute negli oggetti di cui è stata creata un'istanza da questa classe specificano i parametri del file di paging usati quando il file viene creato all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="68e47-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="68e47-106">Le proprietà in questa classe possono essere modificate e rinviate fino all'avvio.</span><span class="sxs-lookup"><span data-stu-id="68e47-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="68e47-107">Queste impostazioni sono diverse dallo stato di run-time di un file di paging espresso tramite la classe associata [**Win32 \_ PageFileUsage**](win32-pagefileusage.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="68e47-108">Per creare un'istanza di questa classe, abilitare il privilegio **SeCreatePagefilePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="68e47-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="68e47-109">Per altre informazioni, vedere [**costanti Privilege**](../wmisdk/privilege-constants.md) ed [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="68e47-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="68e47-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68e47-111">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="68e47-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e47-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68e47-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="68e47-113">Members</span><span class="sxs-lookup"><span data-stu-id="68e47-113">Members</span></span>

<span data-ttu-id="68e47-114">La classe **Win32 \_ PageFileSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="68e47-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="68e47-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68e47-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68e47-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="68e47-116">Properties</span></span>

<span data-ttu-id="68e47-117">La classe **Win32 \_ PageFileSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="68e47-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68e47-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="68e47-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68e47-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68e47-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e47-121">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="68e47-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68e47-122">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="68e47-122">Short textual description of the current object.</span></span>

<span data-ttu-id="68e47-123">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="68e47-124">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="68e47-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68e47-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68e47-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e47-127">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="68e47-127">Textual description of the current object.</span></span>

<span data-ttu-id="68e47-128">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="68e47-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="68e47-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68e47-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="68e47-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68e47-132">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="68e47-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="68e47-133">Dimensioni iniziali del file di paging.</span><span class="sxs-lookup"><span data-stu-id="68e47-133">Initial size of the page file.</span></span>

<span data-ttu-id="68e47-134">Esempio: 139</span><span class="sxs-lookup"><span data-stu-id="68e47-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="68e47-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="68e47-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-136">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68e47-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="68e47-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68e47-138">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**unità**](../wmisdk/standard-qualifiers.md) ("megabyte")</span><span class="sxs-lookup"><span data-stu-id="68e47-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="68e47-139">Dimensioni massime del file di paging.</span><span class="sxs-lookup"><span data-stu-id="68e47-139">Maximum size of the page file.</span></span>

<span data-ttu-id="68e47-140">Esempio: 178</span><span class="sxs-lookup"><span data-stu-id="68e47-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="68e47-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="68e47-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68e47-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="68e47-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68e47-144">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="68e47-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="68e47-145">Percorso e nome file del file di paging.</span><span class="sxs-lookup"><span data-stu-id="68e47-145">Path and file name of the page file.</span></span>

<span data-ttu-id="68e47-146">Esempio: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="68e47-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="68e47-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="68e47-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e47-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="68e47-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e47-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="68e47-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e47-150">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="68e47-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68e47-151">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="68e47-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="68e47-152">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68e47-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="68e47-153">Remarks</span></span>

<span data-ttu-id="68e47-154">La classe **Win32 \_ PageFileSetting** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="68e47-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68e47-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68e47-155">Requirements</span></span>



| <span data-ttu-id="68e47-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e47-156">Requirement</span></span> | <span data-ttu-id="68e47-157">Valore</span><span class="sxs-lookup"><span data-stu-id="68e47-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e47-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68e47-158">Minimum supported client</span></span><br/> | <span data-ttu-id="68e47-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68e47-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68e47-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68e47-160">Minimum supported server</span></span><br/> | <span data-ttu-id="68e47-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68e47-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68e47-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="68e47-162">Namespace</span></span><br/>                | <span data-ttu-id="68e47-163">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="68e47-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68e47-164">MOF</span><span class="sxs-lookup"><span data-stu-id="68e47-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68e47-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68e47-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68e47-166">DLL</span><span class="sxs-lookup"><span data-stu-id="68e47-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e47-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e47-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e47-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68e47-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e47-169">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="68e47-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="68e47-170">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="68e47-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
