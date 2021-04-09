---
description: La \_ classe Win32 DesktopWMI rappresenta le caratteristiche comuni del desktop di un utente. Le proprietà di questa classe possono essere modificate dall'utente per personalizzare il desktop.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Classe Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878362"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="8a8de-104">\_Classe desktop Win32</span><span class="sxs-lookup"><span data-stu-id="8a8de-104">Win32\_Desktop class</span></span>

<span data-ttu-id="8a8de-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) per **\_ desktop Win32** rappresenta le caratteristiche comuni del desktop di un utente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="8a8de-106">Le proprietà di questa classe possono essere modificate dall'utente per personalizzare il desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="8a8de-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8a8de-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8a8de-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8a8de-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a8de-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="8a8de-110">Members</span><span class="sxs-lookup"><span data-stu-id="8a8de-110">Members</span></span>

<span data-ttu-id="8a8de-111">La **classe \_ desktop Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8a8de-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="8a8de-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a8de-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a8de-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a8de-113">Properties</span></span>

<span data-ttu-id="8a8de-114">La **classe \_ desktop Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a8de-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a8de-115">**SpessoreBordo**</span><span class="sxs-lookup"><span data-stu-id="8a8de-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-119">Larghezza dei bordi intorno a tutte le finestre con bordi regolabili.</span><span class="sxs-lookup"><span data-stu-id="8a8de-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="8a8de-120">Esempio: 3</span><span class="sxs-lookup"><span data-stu-id="8a8de-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8a8de-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a8de-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-125">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-125">Short textual description of the current object.</span></span>

<span data-ttu-id="8a8de-126">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8a8de-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-127">**CoolSwitch**</span><span class="sxs-lookup"><span data-stu-id="8a8de-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| CoolSwitch")</span><span class="sxs-lookup"><span data-stu-id="8a8de-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-131">Il cambio rapido delle attività è attivato.</span><span class="sxs-lookup"><span data-stu-id="8a8de-131">Fast task switching is turned on.</span></span> <span data-ttu-id="8a8de-132">Il cambio rapido attività consente all'utente di spostarsi tra le finestre utilizzando la combinazione di tasti **ALT + TAB** .</span><span class="sxs-lookup"><span data-stu-id="8a8de-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-133">**CursorBlinkRate**</span><span class="sxs-lookup"><span data-stu-id="8a8de-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-136">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| CursorBlinkRate"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="8a8de-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-137">Intervallo di tempo tra il cursore successivo lampeggia.</span><span class="sxs-lookup"><span data-stu-id="8a8de-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="8a8de-138">Esempio: 530</span><span class="sxs-lookup"><span data-stu-id="8a8de-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8a8de-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-142">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-142">Textual description of the current object.</span></span>

<span data-ttu-id="8a8de-143">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8a8de-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="8a8de-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| DragFullWindows")</span><span class="sxs-lookup"><span data-stu-id="8a8de-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-148">Il contenuto di una finestra viene visualizzato quando un utente sposta la finestra.</span><span class="sxs-lookup"><span data-stu-id="8a8de-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-149">**GridGranularity**</span><span class="sxs-lookup"><span data-stu-id="8a8de-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-152">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Pannello di controllo \\ \\ Desktop \| GridGranularity"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixel")</span><span class="sxs-lookup"><span data-stu-id="8a8de-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-153">Spaziatura della griglia a cui sono associate le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="8a8de-154">In questo modo l'organizzazione di Windows risulta più semplice.</span><span class="sxs-lookup"><span data-stu-id="8a8de-154">This makes organizing windows easier.</span></span> <span data-ttu-id="8a8de-155">La spaziatura è in genere sufficiente per evitare che l'utente lo noti.</span><span class="sxs-lookup"><span data-stu-id="8a8de-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="8a8de-156">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="8a8de-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="8a8de-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-160">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-161">Spaziatura tra le icone.</span><span class="sxs-lookup"><span data-stu-id="8a8de-161">Spacing between icons.</span></span>

<span data-ttu-id="8a8de-162">Esempio: 75</span><span class="sxs-lookup"><span data-stu-id="8a8de-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-163">**IconTitleFaceName**</span><span class="sxs-lookup"><span data-stu-id="8a8de-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-166">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-167">Tipo di carattere utilizzato per i nomi delle icone.</span><span class="sxs-lookup"><span data-stu-id="8a8de-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="8a8de-168">Esempio: "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="8a8de-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="8a8de-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-172">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| font and text Structures \| [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")</span><span class="sxs-lookup"><span data-stu-id="8a8de-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-173">Dimensioni del carattere dell'icona.</span><span class="sxs-lookup"><span data-stu-id="8a8de-173">Icon font size.</span></span>

<span data-ttu-id="8a8de-174">Esempio: 9</span><span class="sxs-lookup"><span data-stu-id="8a8de-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="8a8de-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-176">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-178">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-179">Il testo del titolo dell'icona viene incapsulato nella riga successiva.</span><span class="sxs-lookup"><span data-stu-id="8a8de-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-180">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8a8de-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-183">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8a8de-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-184">Nome che identifica il profilo desktop corrente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="8a8de-185">Esempio: "MainProf"</span><span class="sxs-lookup"><span data-stu-id="8a8de-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-186">**Modello**</span><span class="sxs-lookup"><span data-stu-id="8a8de-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-189">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Modello di desktop predefinito del \\ \\ Pannello di controllo \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-190">Nome del modello utilizzato come sfondo per il desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="8a8de-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-192">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-194">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaveActive ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-195">Lo screen saver è attivo.</span><span class="sxs-lookup"><span data-stu-id="8a8de-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-196">**ScreenSaverExecutable**</span><span class="sxs-lookup"><span data-stu-id="8a8de-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-199">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\SCRNSAVE.EXE desktop del pannello di controllo predefinito \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-200">Nome del file eseguibile screen saver corrente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="8a8de-201">Esempio: "LOGON. SCR</span><span class="sxs-lookup"><span data-stu-id="8a8de-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="8a8de-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-203">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-205">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaverIsSecure ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-206">La password è abilitata per la screen saver.</span><span class="sxs-lookup"><span data-stu-id="8a8de-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-207">**ScreenSaverTimeout**</span><span class="sxs-lookup"><span data-stu-id="8a8de-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a8de-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-210">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| ScreenSaveTimeOut "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" secondi ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-211">Quantità di tempo che trascorre prima dell'avvio del screen saver.</span><span class="sxs-lookup"><span data-stu-id="8a8de-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="8a8de-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-215">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a8de-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-216">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="8a8de-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="8a8de-217">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8a8de-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-218">**Wallpaper**</span><span class="sxs-lookup"><span data-stu-id="8a8de-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8a8de-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-221">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Sfondo del desktop del pannello di controllo predefinito \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-222">Nome del file per la progettazione dello sfondo sullo sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="8a8de-223">Esempio: "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="8a8de-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-224">**WallpaperStretched**</span><span class="sxs-lookup"><span data-stu-id="8a8de-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-225">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-227">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| WallpaperStyle ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-228">Lo sfondo è allungato per riempire l'intera schermata.</span><span class="sxs-lookup"><span data-stu-id="8a8de-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="8a8de-229">Microsoft Plus</span><span class="sxs-lookup"><span data-stu-id="8a8de-229">Microsoft Plus!</span></span> <span data-ttu-id="8a8de-230">deve essere installato prima che questa opzione sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="8a8de-230">must be installed before this option is available.</span></span> <span data-ttu-id="8a8de-231">Se **false**, lo sfondo mantiene le dimensioni originali sullo sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="8a8de-232">**WallpaperTiled**</span><span class="sxs-lookup"><span data-stu-id="8a8de-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a8de-233">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a8de-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a8de-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a8de-235">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Pannello di controllo predefinito \\ \\ Desktop \| TileWallpaper ")</span><span class="sxs-lookup"><span data-stu-id="8a8de-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="8a8de-236">Lo sfondo è affiancato o centrato.</span><span class="sxs-lookup"><span data-stu-id="8a8de-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a8de-237">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a8de-237">Remarks</span></span>

<span data-ttu-id="8a8de-238">La **classe \_ desktop Win32** è derivata dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="8a8de-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="8a8de-239">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a8de-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="8a8de-240">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="8a8de-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="8a8de-241">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="8a8de-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="8a8de-242">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a8de-242">Examples</span></span>

<span data-ttu-id="8a8de-243">Nell'esempio di codice seguente viene descritto come recuperare le informazioni sul desktop.</span><span class="sxs-lookup"><span data-stu-id="8a8de-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="8a8de-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a8de-244">Requirements</span></span>



| <span data-ttu-id="8a8de-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8de-245">Requirement</span></span> | <span data-ttu-id="8a8de-246">Valore</span><span class="sxs-lookup"><span data-stu-id="8a8de-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8de-247">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a8de-247">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8de-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a8de-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a8de-249">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a8de-249">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8de-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a8de-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a8de-251">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a8de-251">Namespace</span></span><br/>                | <span data-ttu-id="8a8de-252">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8a8de-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a8de-253">MOF</span><span class="sxs-lookup"><span data-stu-id="8a8de-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a8de-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a8de-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a8de-255">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8de-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8de-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8de-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8de-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a8de-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8de-258">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="8a8de-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="8a8de-259">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a8de-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

