---
description: Win32 \_ QuickFixEngineering&\# 8194; La classe WMI rappresenta un piccolo aggiornamento a livello di sistema, comunemente noto come aggiornamento QFE (Quick-Fix Engineering), applicato al sistema operativo corrente.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Classe Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9db31dd452161a31575b6f7184a34c35dea71e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304505"
---
# <a name="win32_quickfixengineering-class"></a><span data-ttu-id="a37b5-103">Win32 \_ QuickFixEngineering (classe)</span><span class="sxs-lookup"><span data-stu-id="a37b5-103">Win32\_QuickFixEngineering class</span></span>

<span data-ttu-id="a37b5-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering Win32** rappresenta un piccolo aggiornamento a livello di sistema, comunemente noto come aggiornamento QFE (Quick Fix Engineering), applicato al sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="a37b5-104">The **Win32\_QuickFixEngineering** [WMI class](../wmisdk/retrieving-a-class.md) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.</span></span> <span data-ttu-id="a37b5-105">Questa classe restituisce solo gli aggiornamenti forniti da Component Based Servicing (CBS).</span><span class="sxs-lookup"><span data-stu-id="a37b5-105">This class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="a37b5-106">Questi aggiornamenti non sono elencati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a37b5-106">These updates are not listed in the registry.</span></span> <span data-ttu-id="a37b5-107">Gli aggiornamenti forniti da Microsoft Windows Installer (MSI) o dal sito Windows Update ( [https://update.microsoft.com](https://update.microsoft.com/) ) non vengono restituiti da **Win32 \_ QuickFixEngineering**.</span><span class="sxs-lookup"><span data-stu-id="a37b5-107">Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([https://update.microsoft.com](https://update.microsoft.com/)) are not returned by **Win32\_QuickFixEngineering**.</span></span>

<span data-ttu-id="a37b5-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a37b5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a37b5-109">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a37b5-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a37b5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a37b5-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a><span data-ttu-id="a37b5-111">Members</span><span class="sxs-lookup"><span data-stu-id="a37b5-111">Members</span></span>

<span data-ttu-id="a37b5-112">La classe **Win32 \_ QuickFixEngineering** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a37b5-112">The **Win32\_QuickFixEngineering** class has these types of members:</span></span>

-   [<span data-ttu-id="a37b5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a37b5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a37b5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a37b5-114">Properties</span></span>

<span data-ttu-id="a37b5-115">La classe **Win32 \_ QuickFixEngineering** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a37b5-115">The **Win32\_QuickFixEngineering** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a37b5-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a37b5-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-119">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a37b5-119">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a37b5-120">A short textual description of the object.</span></span>

<span data-ttu-id="a37b5-121">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-122">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a37b5-122">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-125">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")</span><span class="sxs-lookup"><span data-stu-id="a37b5-125">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-126">Nome locale del computer.</span><span class="sxs-lookup"><span data-stu-id="a37b5-126">Local name of the computer system.</span></span> <span data-ttu-id="a37b5-127">Il valore di questa proprietà deriva dalla classe [**CIM \_ ComputerSystem**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a37b5-127">The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-128">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a37b5-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-131">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a37b5-131">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-132">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a37b5-132">A textual description of the object.</span></span>

<span data-ttu-id="a37b5-133">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-134">**FixComments**</span><span class="sxs-lookup"><span data-stu-id="a37b5-134">**FixComments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="a37b5-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-138">Commenti aggiuntivi relativi all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a37b5-138">Additional comments that relate to the update.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-139">**HotFixID**</span><span class="sxs-lookup"><span data-stu-id="a37b5-139">**HotFixID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-142">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="a37b5-142">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-143">Identificatore univoco associato a un particolare aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a37b5-143">Unique identifier associated with a particular update.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a37b5-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-145">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a37b5-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-147">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a37b5-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-148">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a37b5-148">Indicates when the object was installed.</span></span> <span data-ttu-id="a37b5-149">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a37b5-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a37b5-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-151">**InstalledBy**</span><span class="sxs-lookup"><span data-stu-id="a37b5-151">**InstalledBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-154">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="a37b5-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-155">Persona che ha installato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a37b5-155">Person who installed the update.</span></span> <span data-ttu-id="a37b5-156">Se questo valore è sconosciuto, la proprietà è vuota.</span><span class="sxs-lookup"><span data-stu-id="a37b5-156">If this value is unknown, the property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-157">**InstalledOn**</span><span class="sxs-lookup"><span data-stu-id="a37b5-157">**InstalledOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-160">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="a37b5-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-161">Data di installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a37b5-161">Date that the update was installed.</span></span> <span data-ttu-id="a37b5-162">Se questo valore è sconosciuto, la proprietà è vuota.</span><span class="sxs-lookup"><span data-stu-id="a37b5-162">If this value is unknown, the property is empty.</span></span>

> [!Note]  
> <span data-ttu-id="a37b5-163">Questa proprietà può usare formati diversi, a seconda del momento in cui è stato installato QuickFix.</span><span class="sxs-lookup"><span data-stu-id="a37b5-163">This property may use different formats, depending on when the QuickFix was installed.</span></span> <span data-ttu-id="a37b5-164">Per la maggior parte dei sistemi viene utilizzato un formato di data standard, ad esempio "23-10-2013".</span><span class="sxs-lookup"><span data-stu-id="a37b5-164">Most systems use a standard date format, such as "23-10-2013".</span></span> <span data-ttu-id="a37b5-165">Tuttavia, alcuni sistemi possono restituire un valore esadecimali a 64 bit nel formato Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="a37b5-165">However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

 

</dd> <dt>

<span data-ttu-id="a37b5-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a37b5-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-169">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a37b5-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-170">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a37b5-170">Label by which the object is known.</span></span> <span data-ttu-id="a37b5-171">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a37b5-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a37b5-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-173">**ServicePackInEffect**</span><span class="sxs-lookup"><span data-stu-id="a37b5-173">**ServicePackInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-176">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ hotfix")</span><span class="sxs-lookup"><span data-stu-id="a37b5-176">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-177">Service Pack attivo quando è stato applicato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a37b5-177">Service pack in effect when the update was applied.</span></span> <span data-ttu-id="a37b5-178">Se non è stato applicato alcun Service Pack, la proprietà assume il valore SP0.</span><span class="sxs-lookup"><span data-stu-id="a37b5-178">If no service pack has been applied, the property takes on the value SP0.</span></span> <span data-ttu-id="a37b5-179">Se non è possibile determinare quale Service Pack era attivo, questa proprietà è **null**.</span><span class="sxs-lookup"><span data-stu-id="a37b5-179">If it cannot be determined what service pack was in effect, this property is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a37b5-180">**Status**</span><span class="sxs-lookup"><span data-stu-id="a37b5-180">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a37b5-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a37b5-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a37b5-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a37b5-183">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a37b5-183">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a37b5-184">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a37b5-184">String that indicates the current status of the object.</span></span> <span data-ttu-id="a37b5-185">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a37b5-185">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a37b5-186">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a37b5-186">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a37b5-187">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a37b5-187">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a37b5-188">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a37b5-188">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a37b5-189">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a37b5-189">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a37b5-190">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a37b5-190">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a37b5-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a37b5-192">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a37b5-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a37b5-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a37b5-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a37b5-194">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a37b5-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a37b5-195">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a37b5-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a37b5-196">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a37b5-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a37b5-197">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a37b5-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a37b5-198">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a37b5-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a37b5-199">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a37b5-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a37b5-200">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a37b5-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a37b5-201">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a37b5-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a37b5-202">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a37b5-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a37b5-203">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a37b5-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a37b5-204">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a37b5-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a37b5-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a37b5-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a37b5-206">Commenti</span><span class="sxs-lookup"><span data-stu-id="a37b5-206">Remarks</span></span>

<span data-ttu-id="a37b5-207">La classe **Win32 \_ QuickFixEngineering** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a37b5-207">The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a37b5-208">Poiché gli aggiornamenti vengono archiviati in due posizioni, un'enumerazione di questa classe può generare duplicati.</span><span class="sxs-lookup"><span data-stu-id="a37b5-208">Because updates are stored in two places, an enumeration of this class can result in duplicates.</span></span>

<span data-ttu-id="a37b5-209">Una correzione a caldo è una patch temporanea del sistema operativo prodotta dal gruppo di progettazione Quick Fix in Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a37b5-209">A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft.</span></span> <span data-ttu-id="a37b5-210">Analogamente ai Service Pack, le correzioni rapide rappresentano le modifiche apportate a una versione di Windows dopo il rilascio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a37b5-210">Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.</span></span>

<span data-ttu-id="a37b5-211">A differenza dei Service Pack, le correzioni rapide non sono destinate all'installazione coperta in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="a37b5-211">Unlike service packs, hot fixes are not intended for blanket installation on all computers.</span></span> <span data-ttu-id="a37b5-212">Vengono invece sviluppate per risolvere problemi molto specifici, spesso per configurazioni di computer specifiche.</span><span class="sxs-lookup"><span data-stu-id="a37b5-212">Instead, they are developed to address very specific problems, often for specific computer configurations.</span></span>

<span data-ttu-id="a37b5-213">Inoltre, le correzioni rapide rappresentano installazioni indipendenti che non dipendono da altre correzioni rapide rilasciate.</span><span class="sxs-lookup"><span data-stu-id="a37b5-213">In addition, hot fixes represent independent installations that do not depend on other released hot fixes.</span></span> <span data-ttu-id="a37b5-214">Ad esempio, un ipotetico correzione a caldo 4 non include le correzioni di bug e le funzionalità incluse negli hotfix 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="a37b5-214">For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3.</span></span> <span data-ttu-id="a37b5-215">Nella maggior parte dei casi, non è necessario installare le correzioni rapide 1, 2 e 3 prima di installare Hot Fix 4.</span><span class="sxs-lookup"><span data-stu-id="a37b5-215">In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4.</span></span> <span data-ttu-id="a37b5-216">In questo modo l'enumerazione dei singoli aggiornamenti rapidi è un'attività amministrativa importante: per comprendere la configurazione esatta di un computer, è necessario individuare non solo i Service Pack installati, ma anche i singoli aggiornamenti rapidi installati.</span><span class="sxs-lookup"><span data-stu-id="a37b5-216">This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.</span></span>

<span data-ttu-id="a37b5-217">La classe **Win32 \_ QuickFixEngineering** consente di enumerare tutti gli aggiornamenti rapidi installati in un computer</span><span class="sxs-lookup"><span data-stu-id="a37b5-217">The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer</span></span>

## <a name="examples"></a><span data-ttu-id="a37b5-218">Esempio</span><span class="sxs-lookup"><span data-stu-id="a37b5-218">Examples</span></span>

<span data-ttu-id="a37b5-219">L'esempio di installazione di PowerShell [programmi installati](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) restituisce un elenco completo dei programmi installati.</span><span class="sxs-lookup"><span data-stu-id="a37b5-219">The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.</span></span>

<span data-ttu-id="a37b5-220">Nell'esempio VBScript seguente vengono enumerati gli aggiornamenti rapidi installati in un computer</span><span class="sxs-lookup"><span data-stu-id="a37b5-220">The following VBScript sample enumerates the installed hot fixes on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a><span data-ttu-id="a37b5-221">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37b5-221">Requirements</span></span>



| <span data-ttu-id="a37b5-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="a37b5-222">Requirement</span></span> | <span data-ttu-id="a37b5-223">Valore</span><span class="sxs-lookup"><span data-stu-id="a37b5-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a37b5-224">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a37b5-224">Minimum supported client</span></span><br/> | <span data-ttu-id="a37b5-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a37b5-225">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a37b5-226">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a37b5-226">Minimum supported server</span></span><br/> | <span data-ttu-id="a37b5-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a37b5-227">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a37b5-228">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a37b5-228">Namespace</span></span><br/>                | <span data-ttu-id="a37b5-229">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a37b5-229">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a37b5-230">MOF</span><span class="sxs-lookup"><span data-stu-id="a37b5-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a37b5-231"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a37b5-231"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a37b5-232">DLL</span><span class="sxs-lookup"><span data-stu-id="a37b5-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a37b5-233"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a37b5-233"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a37b5-234">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a37b5-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37b5-235">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a37b5-235">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a37b5-236">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a37b5-236">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a37b5-237">Attività WMI: sistemi operativi</span><span class="sxs-lookup"><span data-stu-id="a37b5-237">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
