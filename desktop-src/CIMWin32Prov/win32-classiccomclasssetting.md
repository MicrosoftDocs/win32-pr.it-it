---
description: Rappresenta le impostazioni di un componente Component Object Model (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305098"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="0e54d-103">Win32 \_ ClassicCOMClassSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="0e54d-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="0e54d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSetting Win32** rappresenta le impostazioni di un componente Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="0e54d-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="0e54d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0e54d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e54d-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0e54d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e54d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e54d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="0e54d-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e54d-108">Members</span></span>

<span data-ttu-id="0e54d-109">La classe **Win32 \_ ClassicCOMClassSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e54d-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0e54d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e54d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e54d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e54d-111">Properties</span></span>

<span data-ttu-id="0e54d-112">La classe **Win32 \_ ClassicCOMClassSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e54d-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e54d-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="0e54d-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-116">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-117">Identificatore univoco globale (GUID) per l'applicazione COM che utilizza questo componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-118">**AutoConvertToClsid**</span><span class="sxs-lookup"><span data-stu-id="0e54d-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-121">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-122">GUID della classe COM in cui verrà convertito automaticamente il componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="0e54d-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-126">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ autotreats \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-127">GUID per il componente COM che emula automaticamente le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="0e54d-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-128">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0e54d-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-131">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0e54d-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-132">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0e54d-132">Short textual description of the current object.</span></span>

<span data-ttu-id="0e54d-133">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0e54d-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="0e54d-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-137">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Class \\ \\ CLSID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-138">GUID di questo componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-139">**Controllo**</span><span class="sxs-lookup"><span data-stu-id="0e54d-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e54d-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-142">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ controllo")</span><span class="sxs-lookup"><span data-stu-id="0e54d-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-143">Il componente COM è un controllo OLE.</span><span class="sxs-lookup"><span data-stu-id="0e54d-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="0e54d-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-148">Percorso del file eseguibile e dell'identificatore di risorsa dell'icona predefinita utilizzata dalla classe.</span><span class="sxs-lookup"><span data-stu-id="0e54d-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-149">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0e54d-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-152">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0e54d-152">Textual description of the current object.</span></span>

<span data-ttu-id="0e54d-153">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0e54d-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="0e54d-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-157">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-158">Percorso completo, incluso FileName o solo filename, per un gestore personalizzato a 16 bit per il componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="0e54d-159">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="0e54d-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-163">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-164">Percorso completo, incluso FileName o solo filename, per un gestore personalizzato a 32 bit per il componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="0e54d-165">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="0e54d-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-169">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-170">Percorso completo, incluso il nome file o solo il nome file, a una DLL del server in-process a 16 bit per questo componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="0e54d-171">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="0e54d-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-175">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-176">Percorso completo, incluso FileName o solo filename, in una DLL del server in-process a 32 bit per questo componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="0e54d-177">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-178">**Inseribile**</span><span class="sxs-lookup"><span data-stu-id="0e54d-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-179">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e54d-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-181">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")</span><span class="sxs-lookup"><span data-stu-id="0e54d-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-182">Il componente COM può essere inserito in applicazioni contenitore OLE.</span><span class="sxs-lookup"><span data-stu-id="0e54d-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-183">**JavaClass**</span><span class="sxs-lookup"><span data-stu-id="0e54d-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-184">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e54d-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-186">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-187">Il componente COM è un componente Java.</span><span class="sxs-lookup"><span data-stu-id="0e54d-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="0e54d-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-191">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-192">Percorso completo, incluso FileName o solo filename, in un'applicazione server locale a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0e54d-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="0e54d-193">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="0e54d-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-197">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-198">Percorso completo, incluso FileName o solo filename, in un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0e54d-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="0e54d-199">Il provider non restituisce sempre il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="0e54d-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0e54d-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-203">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-204">Nome completo dell'applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-204">Full name of the COM application.</span></span> <span data-ttu-id="0e54d-205">Viene utilizzato in aree come il campo dei **risultati** della finestra di dialogo **OLE Incolla speciale** .</span><span class="sxs-lookup"><span data-stu-id="0e54d-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-206">**ProgId**</span><span class="sxs-lookup"><span data-stu-id="0e54d-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-209">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-210">Identificatore a livello di codice associato al componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="0e54d-211">Il formato di un ProgID è <vendor. <Component. <Version.</span><span class="sxs-lookup"><span data-stu-id="0e54d-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="0e54d-212">Questo identificatore non è necessariamente univoco.</span><span class="sxs-lookup"><span data-stu-id="0e54d-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0e54d-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-216">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0e54d-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-217">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0e54d-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="0e54d-218">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0e54d-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0e54d-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-222">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-223">Nome breve dell'applicazione COM (usato nei menu e nei popup).</span><span class="sxs-lookup"><span data-stu-id="0e54d-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="0e54d-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-227">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-228">Modello di threading utilizzato dalle classi COM in-process.</span><span class="sxs-lookup"><span data-stu-id="0e54d-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="0e54d-229">Se questa proprietà è **null**, non viene utilizzato alcun modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="0e54d-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="0e54d-230">Il componente viene creato nel thread principale del client e viene effettuato il marshalling di chiamate da altri thread a questo thread.</span><span class="sxs-lookup"><span data-stu-id="0e54d-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="0e54d-231">Il modello di Apartment specifica che i componenti possono essere immessi da un solo thread.</span><span class="sxs-lookup"><span data-stu-id="0e54d-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="0e54d-232">I dati comuni utilizzati da questi tipi di server degli oggetti devono essere protetti da conflitti di thread perché il server oggetti supporta più componenti.</span><span class="sxs-lookup"><span data-stu-id="0e54d-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="0e54d-233">Ogni componente può essere inserito simultaneamente da thread diversi.</span><span class="sxs-lookup"><span data-stu-id="0e54d-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="0e54d-234">Il modello gratuito specifica che i componenti non inseriscono alcuna restrizione sui thread o sul numero di thread che possono accedere all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e54d-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="0e54d-235">L'oggetto non può contenere dati specifici dei thread e deve proteggere i dati dall'accesso simultaneo da parte di più thread.</span><span class="sxs-lookup"><span data-stu-id="0e54d-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="0e54d-236">Non è tuttavia possibile accedere ai componenti a thread libero direttamente dai thread di Apartment e viene effettuato il marshalling delle chiamate a tali componenti dall'Apartment client.</span><span class="sxs-lookup"><span data-stu-id="0e54d-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="0e54d-237">Quando si specifica both, i componenti possono essere utilizzati in modalità con threading Apartment o a thread libero.</span><span class="sxs-lookup"><span data-stu-id="0e54d-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="0e54d-238">Questi componenti possono essere immessi da più thread, proteggere i dati dai conflitti di thread e non contengono dati specifici del thread.</span><span class="sxs-lookup"><span data-stu-id="0e54d-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="0e54d-239">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="0e54d-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="0e54d-240">Apartment</span><span class="sxs-lookup"><span data-stu-id="0e54d-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="0e54d-241">Libero</span><span class="sxs-lookup"><span data-stu-id="0e54d-241">"Free"</span></span></dd> <dd><span data-ttu-id="0e54d-242">Sia</span><span class="sxs-lookup"><span data-stu-id="0e54d-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="0e54d-243">**Apartment** ("Apartment")</span><span class="sxs-lookup"><span data-stu-id="0e54d-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="0e54d-244">**Gratuito** ("gratuito")</span><span class="sxs-lookup"><span data-stu-id="0e54d-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="0e54d-245">**Both** ("both")</span><span class="sxs-lookup"><span data-stu-id="0e54d-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e54d-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="0e54d-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-249">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolboxBitmap32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-250">Nome del modulo e identificatore di risorsa per una bitmap piccola (16x16) usata per la superficie di un pulsante della barra degli strumenti o della casella degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0e54d-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="0e54d-251">Utilizzato quando il componente COM è un controllo OLE o ActiveX.</span><span class="sxs-lookup"><span data-stu-id="0e54d-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="0e54d-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-255">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Treats \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-256">GUID di un componente COM in grado di emulare le istanze di questo componente.</span><span class="sxs-lookup"><span data-stu-id="0e54d-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="0e54d-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-260">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-261">GUID della libreria dei tipi per il componente COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-262">**Versione**</span><span class="sxs-lookup"><span data-stu-id="0e54d-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-265">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ \\ \\ le classi software del computer locale \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ versione \[ predefinita \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-266">Numero di versione della classe COM.</span><span class="sxs-lookup"><span data-stu-id="0e54d-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="0e54d-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="0e54d-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e54d-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0e54d-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e54d-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e54d-270">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ classs \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgID \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="0e54d-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0e54d-271">Identificatore del programma coerente per tutte le versioni dello stesso programma.</span><span class="sxs-lookup"><span data-stu-id="0e54d-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e54d-272">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e54d-272">Remarks</span></span>

<span data-ttu-id="0e54d-273">La classe **Win32 \_ ClassicCOMClassSetting** è derivata dalla [**\_ comimpostazione Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="0e54d-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e54d-274">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e54d-274">Requirements</span></span>



| <span data-ttu-id="0e54d-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e54d-275">Requirement</span></span> | <span data-ttu-id="0e54d-276">Valore</span><span class="sxs-lookup"><span data-stu-id="0e54d-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e54d-277">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e54d-277">Minimum supported client</span></span><br/> | <span data-ttu-id="0e54d-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e54d-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e54d-279">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e54d-279">Minimum supported server</span></span><br/> | <span data-ttu-id="0e54d-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e54d-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e54d-281">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e54d-281">Namespace</span></span><br/>                | <span data-ttu-id="0e54d-282">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0e54d-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e54d-283">MOF</span><span class="sxs-lookup"><span data-stu-id="0e54d-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e54d-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e54d-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e54d-285">DLL</span><span class="sxs-lookup"><span data-stu-id="0e54d-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e54d-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e54d-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e54d-287">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e54d-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e54d-288">**Comimpostazioni Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0e54d-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="0e54d-289">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e54d-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

