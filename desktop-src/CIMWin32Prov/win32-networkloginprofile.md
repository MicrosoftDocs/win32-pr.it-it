---
description: Win32 \_ NetworkLoginProfile&\# 8194; La classe WMI rappresenta le informazioni di accesso di rete di un utente specifico in un sistema di computer che esegue Windows.
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Classe Win32_NetworkLoginProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b138ce4bc92088896286f4a21a039b068e2206e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305164"
---
# <a name="win32_networkloginprofile-class"></a><span data-ttu-id="10ada-103">Win32 \_ NetworkLoginProfile (classe)</span><span class="sxs-lookup"><span data-stu-id="10ada-103">Win32\_NetworkLoginProfile class</span></span>

<span data-ttu-id="10ada-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkLoginProfile Win32** rappresenta le informazioni di accesso di rete di un utente specifico in un computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="10ada-104">The **Win32\_NetworkLoginProfile** [WMI class](../wmisdk/retrieving-a-class.md) represents the network login information of a specific user on a computer system running Windows.</span></span> <span data-ttu-id="10ada-105">Sono inclusi, ad esempio, lo stato delle password, i privilegi di accesso, le quote disco e i percorsi della directory di accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-105">This includes, but is not limited to password status, access privileges, disk quotas, and logon directory paths.</span></span>

<span data-ttu-id="10ada-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="10ada-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ada-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10ada-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a><span data-ttu-id="10ada-108">Members</span><span class="sxs-lookup"><span data-stu-id="10ada-108">Members</span></span>

<span data-ttu-id="10ada-109">La classe **Win32 \_ NetworkLoginProfile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="10ada-109">The **Win32\_NetworkLoginProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="10ada-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10ada-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10ada-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10ada-111">Properties</span></span>

<span data-ttu-id="10ada-112">La classe **Win32 \_ NetworkLoginProfile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="10ada-112">The **Win32\_NetworkLoginProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10ada-113">**AccountExpires**</span><span class="sxs-lookup"><span data-stu-id="10ada-113">**AccountExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-114">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ada-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Acct \_ scade")</span><span class="sxs-lookup"><span data-stu-id="10ada-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_acct\_expires")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-117">L'account scadrà.</span><span class="sxs-lookup"><span data-stu-id="10ada-117">Account will expire.</span></span> <span data-ttu-id="10ada-118">Questo valore viene calcolato dal numero di secondi trascorsi dal 00:00:00 al 1 gennaio 1970 e viene impostato nel formato seguente: ad aaaammgghhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="10ada-118">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970, and is set in this format: yyyymmddhhmmss.mmmmmm sutc.</span></span>

<span data-ttu-id="10ada-119">Esempio: 20521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="10ada-119">Example: 20521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="10ada-120">**AuthorizationFlags**</span><span class="sxs-lookup"><span data-stu-id="10ada-120">**AuthorizationFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-123">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ Flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span><span class="sxs-lookup"><span data-stu-id="10ada-123">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_auth\_flags"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Printer", "Communication", "Server", "Accounts")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-124">Set di flag che specificano le risorse che un utente è autorizzato a utilizzare o modificare.</span><span class="sxs-lookup"><span data-stu-id="10ada-124">Set of flags that specify the resources a user is authorized to use or modify.</span></span>

<dt>

<span data-ttu-id="10ada-125">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="10ada-125">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-126">Stampante</span><span class="sxs-lookup"><span data-stu-id="10ada-126">Printer</span></span>

</dd> <dt>

<span data-ttu-id="10ada-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="10ada-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-128">Comunicazione</span><span class="sxs-lookup"><span data-stu-id="10ada-128">Communication</span></span>

</dd> <dt>

<span data-ttu-id="10ada-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="10ada-129">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-130">Server</span><span class="sxs-lookup"><span data-stu-id="10ada-130">Server</span></span>

</dd> <dt>

<span data-ttu-id="10ada-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="10ada-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-132">Account</span><span class="sxs-lookup"><span data-stu-id="10ada-132">Accounts</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10ada-133">**BadPasswordCount**</span><span class="sxs-lookup"><span data-stu-id="10ada-133">**BadPasswordCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-136">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Functions \| NetUserEnum")</span><span class="sxs-lookup"><span data-stu-id="10ada-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|NetUserEnum")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-137">Numero di volte in cui l'utente immette una password errata durante l'accesso a un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="10ada-137">Number of times the user enters a bad password when logging on to a computer system running Windows.</span></span>

<span data-ttu-id="10ada-138">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="10ada-138">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="10ada-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="10ada-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-142">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="10ada-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10ada-143">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="10ada-143">Short textual description of the current object.</span></span>

<span data-ttu-id="10ada-144">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-144">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ada-145">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="10ada-145">**CodePage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-148">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ tabella codici \_ ")</span><span class="sxs-lookup"><span data-stu-id="10ada-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_code\_page")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-149">Tabella codici per la lingua scelta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-149">Code page for the user's language of choice.</span></span> <span data-ttu-id="10ada-150">Una tabella codici è il set di caratteri utilizzato.</span><span class="sxs-lookup"><span data-stu-id="10ada-150">A code page is the character set used.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-151">**Commento**</span><span class="sxs-lookup"><span data-stu-id="10ada-151">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-154">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ commento")</span><span class="sxs-lookup"><span data-stu-id="10ada-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-155">Commento o descrizione per questo profilo di accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-155">Comment or description for this logon profile.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-156">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="10ada-156">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-159">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Country \_ Code")</span><span class="sxs-lookup"><span data-stu-id="10ada-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_country\_code")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-160">Codice paese/area geografica per la lingua scelta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-160">Country/region code for the user's language of choice.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-161">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="10ada-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ada-164">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="10ada-164">Textual description of the current object.</span></span>

<span data-ttu-id="10ada-165">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-165">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ada-166">**Flag**</span><span class="sxs-lookup"><span data-stu-id="10ada-166">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-169">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags"), [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("script", "Account disabled", "Home dir required", "lockout", "password non obbligatoria", "Paswword Can Change", "Encrypted test password allowed", "Temp duplicate account", "Normal account", "account trust tra domini", "account di attendibilità della workstation", "account di attendibilità del server", "senza scadenza password", "account di accesso MNS", "smartcard obbligatoria", "trusted per la delega", "non delegata", "USA solo chiave des", "non richiedere la preautorizzazione", "password scaduta")</span><span class="sxs-lookup"><span data-stu-id="10ada-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags"), [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "3", "4", "5", "6", "7", "8", "9", "11", "12", "13", "16", "17", "18", "19", "20", "21", "22", "23"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Script", "Account Disabled", "Home Dir Required", "Lockout", "Password Not Required", "Paswword Can't Change", "Encrypted Test Password Allowed", "Temp Duplicate Account", "Normal Account", "InterDomain Trust Account", "WorkStation Trust Account", "Server Trust Account", "Don't Expire Password", "MNS Logon Account", "Smartcard Required", "Trusted For Delegation", "Not Delegated", "Use DES Key Only", "Don't Require Preauthorization", "Password Expired")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-170">Proprietà disponibili per questo profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="10ada-170">The properties available to this network profile.</span></span>

<span data-ttu-id="10ada-171">Le proprietà che è possibile impostare includono:</span><span class="sxs-lookup"><span data-stu-id="10ada-171">Properties that can be set include:</span></span>

<dt>

<span data-ttu-id="10ada-172">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="10ada-172">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-173">Script</span><span class="sxs-lookup"><span data-stu-id="10ada-173">Script</span></span>

<span data-ttu-id="10ada-174">Uno script di accesso eseguito.</span><span class="sxs-lookup"><span data-stu-id="10ada-174">A logon script executed.</span></span> <span data-ttu-id="10ada-175">Questo valore deve essere impostato per LAN Manager 2,0.</span><span class="sxs-lookup"><span data-stu-id="10ada-175">This value must be set for LAN Manager 2.0.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-176">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="10ada-176">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-177">Account disabilitato</span><span class="sxs-lookup"><span data-stu-id="10ada-177">Account Disabled</span></span>

<span data-ttu-id="10ada-178">L'account dell'utente è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="10ada-178">The user's account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-179">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="10ada-179">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-180">Home directory obbligatoria</span><span class="sxs-lookup"><span data-stu-id="10ada-180">Home Directory Required</span></span>

<span data-ttu-id="10ada-181">È necessaria una home directory.</span><span class="sxs-lookup"><span data-stu-id="10ada-181">A home directory is required.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-182">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="10ada-182">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-183">Blocco</span><span class="sxs-lookup"><span data-stu-id="10ada-183">Lockout</span></span>

<span data-ttu-id="10ada-184">L'account è attualmente bloccato. Per [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), questo valore può essere cancellato per sbloccare un account bloccato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="10ada-184">The account is currently locked out. For [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo), this value can be cleared to unlock a previously locked account.</span></span> <span data-ttu-id="10ada-185">Questo valore non può essere usato per bloccare un account precedentemente sbloccato.</span><span class="sxs-lookup"><span data-stu-id="10ada-185">This value cannot be used to lock a previously unlocked account.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-186">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="10ada-186">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-187">Password non richiesta</span><span class="sxs-lookup"><span data-stu-id="10ada-187">Password Not Required</span></span>

<span data-ttu-id="10ada-188">Non è necessaria alcuna password.</span><span class="sxs-lookup"><span data-stu-id="10ada-188">No password is required.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-189">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="10ada-189">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-190">Impossibile modificare la password</span><span class="sxs-lookup"><span data-stu-id="10ada-190">Password Cannot Change</span></span>

<span data-ttu-id="10ada-191">L'utente non può modificare la password.</span><span class="sxs-lookup"><span data-stu-id="10ada-191">The user cannot change the password.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-192">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="10ada-192">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-193">Password di test crittografata consentita</span><span class="sxs-lookup"><span data-stu-id="10ada-193">Encrypted Test Password Allowed</span></span>

</dd> <dt>

<span data-ttu-id="10ada-194">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="10ada-194">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-195">Account duplicato temporaneo</span><span class="sxs-lookup"><span data-stu-id="10ada-195">Temp Duplicate Account</span></span>

<span data-ttu-id="10ada-196">Un account per gli utenti il cui account primario si trova in un altro dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-196">An account for users whose primary account is in another domain.</span></span> <span data-ttu-id="10ada-197">Questo account fornisce l'accesso utente al dominio, ma non a un dominio che considera attendibile il dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-197">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="10ada-198">Il gestore utenti fa riferimento a questo tipo di account come account utente locale.</span><span class="sxs-lookup"><span data-stu-id="10ada-198">The User Manager refers to this account type as a local user account.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-199">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="10ada-199">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-200">Account normale</span><span class="sxs-lookup"><span data-stu-id="10ada-200">Normal Account</span></span>

<span data-ttu-id="10ada-201">Tipo di account predefinito che rappresenta un utente tipico.</span><span class="sxs-lookup"><span data-stu-id="10ada-201">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-202">2048 (0x800)</span><span class="sxs-lookup"><span data-stu-id="10ada-202">2048 (0x800)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-203">Account trust tra domini</span><span class="sxs-lookup"><span data-stu-id="10ada-203">Interdomain Trust Account</span></span>

<span data-ttu-id="10ada-204">Consentire a un account attendibile per un dominio che considera attendibile altri domini.</span><span class="sxs-lookup"><span data-stu-id="10ada-204">A permit to a trust account for a domain that trusts other domains.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-205">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="10ada-205">4096 (0x1000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-206">Account attendibilità workstation</span><span class="sxs-lookup"><span data-stu-id="10ada-206">Workstation Trust Account</span></span>

<span data-ttu-id="10ada-207">Un account computer per una workstation o un server Windows appartenente a questo dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-207">A computer account for a Windows workstation or server that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-208">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="10ada-208">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-209">Account Trust Server</span><span class="sxs-lookup"><span data-stu-id="10ada-209">Server Trust Account</span></span>

<span data-ttu-id="10ada-210">Un account computer di un controller di dominio di backup che è membro di questo dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-210">A computer account for a backup domain controller that is a member of this domain.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-211">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="10ada-211">65536 (0x10000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-212">Nessuna scadenza password</span><span class="sxs-lookup"><span data-stu-id="10ada-212">Do Not Expire Password</span></span>

</dd> <dt>

<span data-ttu-id="10ada-213">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="10ada-213">131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-214">Account di accesso MNS</span><span class="sxs-lookup"><span data-stu-id="10ada-214">MNS Logon Account</span></span>

<span data-ttu-id="10ada-215">Tipo di account di accesso MNS (Major node set) che rappresenta un utente MNS.</span><span class="sxs-lookup"><span data-stu-id="10ada-215">Majority Node Set (MNS) logon account type that represents an MNS user.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-216">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="10ada-216">262144 (0x40000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-217">Smart Card obbligatoria</span><span class="sxs-lookup"><span data-stu-id="10ada-217">Smartcard Required</span></span>

</dd> <dt>

<span data-ttu-id="10ada-218">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="10ada-218">524288 (0x80000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-219">Attendibile per la delega</span><span class="sxs-lookup"><span data-stu-id="10ada-219">Trusted for Delegation</span></span>

</dd> <dt>

<span data-ttu-id="10ada-220">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="10ada-220">1048576 (0x100000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-221">Non delegato</span><span class="sxs-lookup"><span data-stu-id="10ada-221">Not Delegated</span></span>

</dd> <dt>

<span data-ttu-id="10ada-222">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="10ada-222">2097152 (0x200000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-223">USA solo chiave DES</span><span class="sxs-lookup"><span data-stu-id="10ada-223">Use DES Key Only</span></span>

</dd> <dt>

<span data-ttu-id="10ada-224">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="10ada-224">4194304 (0x400000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-225">Non richiedere la preautorizzazione</span><span class="sxs-lookup"><span data-stu-id="10ada-225">Do Not Require Preauthorization</span></span>

</dd> <dt>

<span data-ttu-id="10ada-226">8388608 (0x800000)</span><span class="sxs-lookup"><span data-stu-id="10ada-226">8388608 (0x800000)</span></span>
</dt> <dd>

<span data-ttu-id="10ada-227">Password scaduta</span><span class="sxs-lookup"><span data-stu-id="10ada-227">Password Expired</span></span>

<span data-ttu-id="10ada-228">Indica che la password è scaduta.</span><span class="sxs-lookup"><span data-stu-id="10ada-228">Indicates that the password has expired.</span></span>

</dd> </dl>

<span data-ttu-id="10ada-229">Le proprietà seguenti descrivono il tipo di account.</span><span class="sxs-lookup"><span data-stu-id="10ada-229">The following properties describe the account type.</span></span> <span data-ttu-id="10ada-230">È possibile impostare un solo valore:</span><span class="sxs-lookup"><span data-stu-id="10ada-230">Only one value can be set:</span></span>

-   <span data-ttu-id="10ada-231">\_account UF Normal \_</span><span class="sxs-lookup"><span data-stu-id="10ada-231">UF\_NORMAL\_ACCOUNT</span></span>
-   <span data-ttu-id="10ada-232">\_account con \_ duplicazione temporanea UF \_</span><span class="sxs-lookup"><span data-stu-id="10ada-232">UF\_TEMP\_DUPLICATE\_ACCOUNT</span></span>
-   <span data-ttu-id="10ada-233">\_ \_ account attendibilità UF workstation \_</span><span class="sxs-lookup"><span data-stu-id="10ada-233">UF\_WORKSTATION\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="10ada-234">\_ \_ account trust server \_ UF</span><span class="sxs-lookup"><span data-stu-id="10ada-234">UF\_SERVER\_TRUST\_ACCOUNT</span></span>
-   <span data-ttu-id="10ada-235">\_ \_ account trust tra domini \_ UF</span><span class="sxs-lookup"><span data-stu-id="10ada-235">UF\_INTERDOMAIN\_TRUST\_ACCOUNT</span></span>

</dd> <dt>

<span data-ttu-id="10ada-236">**FullName**</span><span class="sxs-lookup"><span data-stu-id="10ada-236">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-239">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ nome completo")</span><span class="sxs-lookup"><span data-stu-id="10ada-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_full\_name")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-240">Nome completo dell'utente che appartiene al profilo di accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="10ada-240">Full name of the user belonging to the network login profile.</span></span> <span data-ttu-id="10ada-241">Questa stringa può essere vuota se l'utente sceglie di non associare un nome completo a un nome utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-241">This string can be empty if the user chooses not to associate a full name with a user name.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-242">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="10ada-242">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-245">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir")</span><span class="sxs-lookup"><span data-stu-id="10ada-245">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-246">Percorso della Home directory dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-246">Path to the home directory of the user.</span></span> <span data-ttu-id="10ada-247">Questa stringa può essere vuota se l'utente sceglie di non specificare una home directory.</span><span class="sxs-lookup"><span data-stu-id="10ada-247">This string may be empty if the user chooses not to specify a home directory.</span></span>

<span data-ttu-id="10ada-248">Esempio: " \\ homedir"</span><span class="sxs-lookup"><span data-stu-id="10ada-248">Example:"\\HOMEDIR"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-249">**HomeDirectoryDrive**</span><span class="sxs-lookup"><span data-stu-id="10ada-249">**HomeDirectoryDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-252">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Home \_ dir \_ Drive")</span><span class="sxs-lookup"><span data-stu-id="10ada-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_home\_dir\_drive")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-253">Lettera di unità assegnata alla Home directory dell'utente per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-253">Drive letter assigned to the user's home directory for log on purposes.</span></span>

<span data-ttu-id="10ada-254">Esempio: "C:"</span><span class="sxs-lookup"><span data-stu-id="10ada-254">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-255">**LastLogoff**</span><span class="sxs-lookup"><span data-stu-id="10ada-255">**LastLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-256">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ada-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-258">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Ultima \_ disconnessione")</span><span class="sxs-lookup"><span data-stu-id="10ada-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logoff")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-259">Ultimo accesso dell'utente al sistema.</span><span class="sxs-lookup"><span data-stu-id="10ada-259">User last logged off the system.</span></span> <span data-ttu-id="10ada-260">Questo valore viene calcolato dal numero di secondi trascorsi da 00:00:00, 1 gennaio 1970.</span><span class="sxs-lookup"><span data-stu-id="10ada-260">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="10ada-261">Il valore " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " indica che l'ora dell'ultimo disconnessione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="10ada-261">A value of " \*\*\*\*\*\*\*\*\*\*\*\*\*\*.\*\*\*\*\*\*+\*\*\* " means that the last logoff time is unknown.</span></span> <span data-ttu-id="10ada-262">Il formato di questo valore è ad aaaammgghhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="10ada-262">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="10ada-263">Per informazioni sulla conversione di questa proprietà nell'ora locale, vedere [attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-263">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="10ada-264">Esempio: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="10ada-264">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="10ada-265">**LastLogon**</span><span class="sxs-lookup"><span data-stu-id="10ada-265">**LastLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-266">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ada-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-268">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ ultimo \_ accesso")</span><span class="sxs-lookup"><span data-stu-id="10ada-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_last\_logon")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-269">Ultimo accesso dell'utente al sistema.</span><span class="sxs-lookup"><span data-stu-id="10ada-269">User last logged on to the system.</span></span> <span data-ttu-id="10ada-270">Questo valore viene calcolato dal numero di secondi trascorsi da 00:00:00, 1 gennaio 1970.</span><span class="sxs-lookup"><span data-stu-id="10ada-270">This value is calculated from the number of seconds elapsed since 00:00:00, January 1, 1970.</span></span> <span data-ttu-id="10ada-271">Il formato di questo valore è ad aaaammgghhmmss. mmmmmm SUTC.</span><span class="sxs-lookup"><span data-stu-id="10ada-271">The format of this value is yyyymmddhhmmss.mmmmmm sutc.</span></span> <span data-ttu-id="10ada-272">Per informazioni sulla conversione di questa proprietà nell'ora locale, vedere [attività WMI: date e ore](../wmisdk/wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-272">For information about translating this property into your local time, see [WMI Tasks: Dates and Times](../wmisdk/wmi-tasks--dates-and-times.md).</span></span>

<span data-ttu-id="10ada-273">Esempio: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="10ada-273">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="10ada-274">**LogonHours**</span><span class="sxs-lookup"><span data-stu-id="10ada-274">**LogonHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-277">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 ore di \_ accesso \_ ")</span><span class="sxs-lookup"><span data-stu-id="10ada-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (147), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_hours")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-278">Orari durante i quali l'utente può effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-278">Times during the week when the user can log on.</span></span> <span data-ttu-id="10ada-279">Ogni bit rappresenta un'unità di tempo specificata dalla proprietà **UnitsPerWeek** .</span><span class="sxs-lookup"><span data-stu-id="10ada-279">Each bit represents a unit of time specified by the **UnitsPerWeek** property.</span></span> <span data-ttu-id="10ada-280">Ad esempio, se l'unità di tempo è ogni ora, il primo bit (bit 0, Word 0) è domenica, 0:00 a 0:59, il secondo bit (bit 1, Word 0) è domenica, 1:00 a 1:59 e così via.</span><span class="sxs-lookup"><span data-stu-id="10ada-280">For instance, if the unit of time is hourly, the first bit (bit 0, word 0) is Sunday, 0:00 to 0:59, the second bit (bit 1, word 0) is Sunday, 1:00 to 1:59, and so on.</span></span> <span data-ttu-id="10ada-281">Se questo membro è impostato su **null**, non esiste alcuna restrizione temporale.</span><span class="sxs-lookup"><span data-stu-id="10ada-281">If this member is set to **NULL**, then there is no time restriction.</span></span> <span data-ttu-id="10ada-282">L'ora è impostata su GMT e deve essere regolata per altri fusi orari (ad esempio, GMT meno 8 ore per PST).</span><span class="sxs-lookup"><span data-stu-id="10ada-282">The time is set to GMT and must be adjusted for other time zones (for example, GMT minus 8 hours for PST).</span></span>

</dd> <dt>

<span data-ttu-id="10ada-283">**LogonServer**</span><span class="sxs-lookup"><span data-stu-id="10ada-283">**LogonServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-286">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Logon \_ Server")</span><span class="sxs-lookup"><span data-stu-id="10ada-286">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_logon\_server")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-287">Nome del server a cui vengono inviate le richieste di accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-287">Name of the server to which logon requests are sent.</span></span> <span data-ttu-id="10ada-288">I nomi dei server devono essere preceduti da due barre rovesciate ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="10ada-288">Server names should be preceded by two backslashes (\\\\).</span></span> <span data-ttu-id="10ada-289">Il nome di un server con un asterisco ( \\ \\ \* ) indica che la richiesta di accesso può essere gestita da qualsiasi server di accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-289">A server name with an asterisk (\\\\\*) indicates that the logon request can be handled by any logon server.</span></span> <span data-ttu-id="10ada-290">Una stringa null indica che le richieste vengono inviate al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-290">A null string indicates that requests are sent to the domain controller.</span></span>

<span data-ttu-id="10ada-291">Esempio: " \\ \\ MyServer"</span><span class="sxs-lookup"><span data-stu-id="10ada-291">Example: "\\\\MyServer"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-292">**MaximumStorage**</span><span class="sxs-lookup"><span data-stu-id="10ada-292">**MaximumStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-293">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="10ada-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-295">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Max \_ storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="10ada-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_max\_storage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-296">Quantità massima di spazio su disco disponibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-296">Maximum amount of disk space available to the user.</span></span> <span data-ttu-id="10ada-297">Se MaximumStorage è impostato su USER \_ MAXSTORAGE \_ Unlimited, l'utente può usare tutto lo spazio su disco disponibile.</span><span class="sxs-lookup"><span data-stu-id="10ada-297">If MaximumStorage is set to USER\_MAXSTORAGE\_UNLIMITED, the user is allowed to use all of the available disk space.</span></span>

<span data-ttu-id="10ada-298">Esempio: 10 milioni</span><span class="sxs-lookup"><span data-stu-id="10ada-298">Example: 10000000</span></span>

<span data-ttu-id="10ada-299">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="10ada-299">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="10ada-300">**Nome**</span><span class="sxs-lookup"><span data-stu-id="10ada-300">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-301">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-303">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ nome")</span><span class="sxs-lookup"><span data-stu-id="10ada-303">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_name")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-304">Account utente in un dominio o in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="10ada-304">User account on a particular domain or computer.</span></span> <span data-ttu-id="10ada-305">Il numero di caratteri nel nome non può superare il valore di UNLEN.</span><span class="sxs-lookup"><span data-stu-id="10ada-305">The number of characters in the name cannot exceed the value of UNLEN.</span></span>

<span data-ttu-id="10ada-306">Esempio: "somedomain \\ JohnDoe"</span><span class="sxs-lookup"><span data-stu-id="10ada-306">Example: "somedomain\\johndoe"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-307">**NumberOfLogons**</span><span class="sxs-lookup"><span data-stu-id="10ada-307">**NumberOfLogons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-308">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-310">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num \_ accessi")</span><span class="sxs-lookup"><span data-stu-id="10ada-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_num\_logons")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-311">Numero di volte che l'utente ha tentato di accedere a questo account.</span><span class="sxs-lookup"><span data-stu-id="10ada-311">Number of successful times the user tried to log on to this account.</span></span> <span data-ttu-id="10ada-312">Il valore 0xFFFFFFFF indica che il valore è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="10ada-312">A value of 0xFFFFFFFF indicates that the value is unknown.</span></span> <span data-ttu-id="10ada-313">Questa proprietà viene gestita separatamente in ogni controller di dominio di backup (BDC) nel dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-313">This property is maintained separately on each backup domain controller (BDC) in the domain.</span></span> <span data-ttu-id="10ada-314">Per ottenere un valore accurato, è necessario usare solo il valore più grande di tutti i I BDC.</span><span class="sxs-lookup"><span data-stu-id="10ada-314">To get an accurate value, only the largest value from all BDCs should be used.</span></span>

<span data-ttu-id="10ada-315">Example: 4</span><span class="sxs-lookup"><span data-stu-id="10ada-315">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="10ada-316">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="10ada-316">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-319">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parametri")</span><span class="sxs-lookup"><span data-stu-id="10ada-319">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_parms")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-320">Spazio accantonato per l'uso da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="10ada-320">Space set aside for use by applications.</span></span> <span data-ttu-id="10ada-321">Questa stringa può essere null oppure può contenere un numero qualsiasi di caratteri prima del carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="10ada-321">This string can be null, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="10ada-322">I prodotti Microsoft utilizzano questo membro per archiviare le informazioni di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-322">Microsoft products use this member to store user configuration information.</span></span> <span data-ttu-id="10ada-323">Non modificare queste informazioni, poiché questo valore è specifico di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="10ada-323">Do not modify this information, because this value is specific to an application.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-324">**Password**</span><span class="sxs-lookup"><span data-stu-id="10ada-324">**PasswordAge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-325">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ada-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-327">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ password \_ Age")</span><span class="sxs-lookup"><span data-stu-id="10ada-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_password\_age")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-328">Periodo di tempo in cui una password è stata applicata.</span><span class="sxs-lookup"><span data-stu-id="10ada-328">Length of time a password has been in effect.</span></span> <span data-ttu-id="10ada-329">Questo valore viene misurato dal numero di secondi trascorsi dall'Ultima modifica della password.</span><span class="sxs-lookup"><span data-stu-id="10ada-329">This value is measured from the number of seconds elapsed since the password was last changed.</span></span>

<span data-ttu-id="10ada-330">Esempio: 00001201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="10ada-330">Example: 00001201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="10ada-331">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="10ada-331">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-332">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ada-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-334">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ modale \_ info \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ Max \_ passwd \_ Age")</span><span class="sxs-lookup"><span data-stu-id="10ada-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_MODALS\_INFO\_0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0)\|usrmod0\_max\_passwd\_age")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-335">Data e ora di scadenza della password.</span><span class="sxs-lookup"><span data-stu-id="10ada-335">Date and time the password expires.</span></span> <span data-ttu-id="10ada-336">Il valore viene impostato nel formato seguente: ad aaaammgghhmmss. mmmmmm SUTC</span><span class="sxs-lookup"><span data-stu-id="10ada-336">The value is set in this format: yyyymmddhhmmss.mmmmmm sutc</span></span>

<span data-ttu-id="10ada-337">Esempio: 19521201000230,000000 000</span><span class="sxs-lookup"><span data-stu-id="10ada-337">Example: 19521201000230.000000 000</span></span>

</dd> <dt>

<span data-ttu-id="10ada-338">**PrimaryGroupId**</span><span class="sxs-lookup"><span data-stu-id="10ada-338">**PrimaryGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-339">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-341">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ gruppo primario \_ ID")</span><span class="sxs-lookup"><span data-stu-id="10ada-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_primary\_group\_id")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-342">Identificatore relativo (RID) del gruppo globale primario per questo utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-342">Relative identifier (RID) of the Primary Global Group for this user.</span></span> <span data-ttu-id="10ada-343">L'identificatore verifica il gruppo primario a cui appartiene il profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-343">The identifier verifies the primary group to which the user's profile belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-344">**Privilegi**</span><span class="sxs-lookup"><span data-stu-id="10ada-344">**Privileges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-345">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-345">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-347">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ priv")</span><span class="sxs-lookup"><span data-stu-id="10ada-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_priv")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-348">Livello di privilegio assegnato alla proprietà **del \_ nome usri3** .</span><span class="sxs-lookup"><span data-stu-id="10ada-348">Level of privilege assigned to the **usri3\_name** property.</span></span>

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

<span data-ttu-id="10ada-349">**Guest** (0)</span><span class="sxs-lookup"><span data-stu-id="10ada-349">**Guest** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

<span data-ttu-id="10ada-350">**Utente** (1)</span><span class="sxs-lookup"><span data-stu-id="10ada-350">**User** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

<span data-ttu-id="10ada-351">**Amministratore** (2)</span><span class="sxs-lookup"><span data-stu-id="10ada-351">**Administrator** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ada-352">**Profilo**</span><span class="sxs-lookup"><span data-stu-id="10ada-352">**Profile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-355">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ profilo usri3")</span><span class="sxs-lookup"><span data-stu-id="10ada-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_profile")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-356">Percorso del profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-356">Path to the user's profile.</span></span> <span data-ttu-id="10ada-357">Questo valore può essere una stringa null, un percorso assoluto locale o un percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="10ada-357">This value can be a null string, a local absolute path, or a UNC path.</span></span> <span data-ttu-id="10ada-358">Un profilo utente contiene impostazioni personalizzabili per ogni utente, ad esempio i colori del desktop.</span><span class="sxs-lookup"><span data-stu-id="10ada-358">A user profile contains settings that are customizable for each user such as the desktop colors.</span></span>

<span data-ttu-id="10ada-359">Esempio: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="10ada-359">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-360">**ScriptPath**</span><span class="sxs-lookup"><span data-stu-id="10ada-360">**ScriptPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-363">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ percorso script")</span><span class="sxs-lookup"><span data-stu-id="10ada-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_script\_path")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-364">Percorso della directory dello script di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-364">Directory path to the user's logon script.</span></span> <span data-ttu-id="10ada-365">Uno script di accesso esegue automaticamente un set di comandi ogni volta che un utente accede a un sistema.</span><span class="sxs-lookup"><span data-stu-id="10ada-365">A logon script automatically executes a set of commands each time a user logs on to a system.</span></span>

<span data-ttu-id="10ada-366">Esempio: "C: \\ Win \\ profiles \\ ThomasSteven"</span><span class="sxs-lookup"><span data-stu-id="10ada-366">Example: "C:\\win\\profiles\\ThomasSteven"</span></span>

</dd> <dt>

<span data-ttu-id="10ada-367">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="10ada-367">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-368">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-370">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="10ada-370">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="10ada-371">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="10ada-371">Identifier by which the current object is known.</span></span>

<span data-ttu-id="10ada-372">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-372">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ada-373">**UnitsPerWeek**</span><span class="sxs-lookup"><span data-stu-id="10ada-373">**UnitsPerWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-374">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-376">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ unità usri3 \_ alla \_ settimana")</span><span class="sxs-lookup"><span data-stu-id="10ada-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_units\_per\_week")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-377">Numero di unità di tempo in cui la settimana è divisa.</span><span class="sxs-lookup"><span data-stu-id="10ada-377">Number of time units the week is divided into.</span></span> <span data-ttu-id="10ada-378">Viene utilizzato con la proprietà **LogonHours** per limitare l'accesso degli utenti al computer.</span><span class="sxs-lookup"><span data-stu-id="10ada-378">It is used with the **LogonHours** property to limit user access to the computer.</span></span>

<span data-ttu-id="10ada-379">Esempio: 168 (ore alla settimana)</span><span class="sxs-lookup"><span data-stu-id="10ada-379">Example: 168 (hours per week)</span></span>

</dd> <dt>

<span data-ttu-id="10ada-380">**UserComment**</span><span class="sxs-lookup"><span data-stu-id="10ada-380">**UserComment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-383">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ Comment")</span><span class="sxs-lookup"><span data-stu-id="10ada-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_usr\_comment")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-384">Commento o descrizione definito dall'utente per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="10ada-384">User-defined comment or description for this profile.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-385">**UserId**</span><span class="sxs-lookup"><span data-stu-id="10ada-385">**UserId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-386">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10ada-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-388">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ \_ ID utente")</span><span class="sxs-lookup"><span data-stu-id="10ada-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_user\_id")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-389">RID dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10ada-389">RID of the user.</span></span> <span data-ttu-id="10ada-390">L'identificatore verifica che l'utente esista ed è univoco per questo dominio.</span><span class="sxs-lookup"><span data-stu-id="10ada-390">The identifier verifies that the user exists and is unique to this domain.</span></span>

</dd> <dt>

<span data-ttu-id="10ada-391">**UserType**</span><span class="sxs-lookup"><span data-stu-id="10ada-391">**UserType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-392">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-394">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**User \_ info \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ Flags")</span><span class="sxs-lookup"><span data-stu-id="10ada-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-395">Tipo di account per cui l'utente dispone dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="10ada-395">Type of account to which the user has privileges.</span></span>

<span data-ttu-id="10ada-396">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="10ada-396">The values are:</span></span>

-   <span data-ttu-id="10ada-397">"Account normale"</span><span class="sxs-lookup"><span data-stu-id="10ada-397">"Normal Account"</span></span>
-   <span data-ttu-id="10ada-398">"Account duplicato"</span><span class="sxs-lookup"><span data-stu-id="10ada-398">"Duplicate Account"</span></span>
-   <span data-ttu-id="10ada-399">"Account attendibilità workstation"</span><span class="sxs-lookup"><span data-stu-id="10ada-399">"Workstation Trust Account"</span></span>
-   <span data-ttu-id="10ada-400">"Account Trust Server"</span><span class="sxs-lookup"><span data-stu-id="10ada-400">"Server Trust Account"</span></span>
-   <span data-ttu-id="10ada-401">"Account trust tra domini"</span><span class="sxs-lookup"><span data-stu-id="10ada-401">"Interdomain Trust Account"</span></span>
-   <span data-ttu-id="10ada-402">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="10ada-402">"Unknown"</span></span>

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="10ada-403">**Normale account** ("normale account")</span><span class="sxs-lookup"><span data-stu-id="10ada-403">**Normal Account** ("Normal Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="10ada-404">**Account duplicato** ("account duplicato")</span><span class="sxs-lookup"><span data-stu-id="10ada-404">**Duplicate Account** ("Duplicate Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="10ada-405">**Account attendibilità workstation** ("account trust workstation")</span><span class="sxs-lookup"><span data-stu-id="10ada-405">**Workstation Trust Account** ("Workstation Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="10ada-406">**Account trust server** ("account Trust Server")</span><span class="sxs-lookup"><span data-stu-id="10ada-406">**Server Trust Account** ("Server Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="10ada-407">**Account trust tra domini** ("account trust tra domini")</span><span class="sxs-lookup"><span data-stu-id="10ada-407">**Interdomain Trust Account** ("Interdomain Trust Account")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ada-408">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="10ada-408">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ada-409">**Workstation**</span><span class="sxs-lookup"><span data-stu-id="10ada-409">**Workstations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ada-410">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10ada-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ada-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10ada-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ada-412">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**\_ informazioni utente \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ workstation usri3")</span><span class="sxs-lookup"><span data-stu-id="10ada-412">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3)\|usri3\_workstations")</span></span>
</dt> </dl>

<span data-ttu-id="10ada-413">Nomi delle workstation da cui l'utente può effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="10ada-413">Names of workstations from which the user can log on.</span></span> <span data-ttu-id="10ada-414">È possibile specificare fino a otto workstation. i nomi devono essere separati da virgole (,).</span><span class="sxs-lookup"><span data-stu-id="10ada-414">Up to eight workstations can be specified; the names must be separated by commas (,).</span></span> <span data-ttu-id="10ada-415">Una stringa null indica nessuna restrizione.</span><span class="sxs-lookup"><span data-stu-id="10ada-415">A null string indicates no restrictions.</span></span> <span data-ttu-id="10ada-416">Per disabilitare gli accessi da tutte le workstation a questo account, impostare UF \_ ACCOUNTDISABLE nella proprietà **Flags** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="10ada-416">To disable logons from all workstations to this account, set the UF\_ACCOUNTDISABLE in the **Flags** property of this class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10ada-417">Commenti</span><span class="sxs-lookup"><span data-stu-id="10ada-417">Remarks</span></span>

<span data-ttu-id="10ada-418">La classe **Win32 \_ NetworkLoginProfile** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-418">The **Win32\_NetworkLoginProfile** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="10ada-419">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="10ada-419">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="10ada-420">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="10ada-420">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

## <a name="examples"></a><span data-ttu-id="10ada-421">Esempio</span><span class="sxs-lookup"><span data-stu-id="10ada-421">Examples</span></span>

<span data-ttu-id="10ada-422">L'esempio [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell restituisce le informazioni di accesso alla rete per tutti gli utenti di un computer.</span><span class="sxs-lookup"><span data-stu-id="10ada-422">The [List Network Login Profiles](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14) PowerShell sample returns network login information for all the users of a computer.</span></span>

<span data-ttu-id="10ada-423">Nell'esempio VBScript seguente vengono restituite informazioni di accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="10ada-423">The following VBScript sample returns network login information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
```



## <a name="requirements"></a><span data-ttu-id="10ada-424">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10ada-424">Requirements</span></span>



| <span data-ttu-id="10ada-425">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ada-425">Requirement</span></span> | <span data-ttu-id="10ada-426">Valore</span><span class="sxs-lookup"><span data-stu-id="10ada-426">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10ada-427">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10ada-427">Minimum supported client</span></span><br/> | <span data-ttu-id="10ada-428">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10ada-428">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10ada-429">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10ada-429">Minimum supported server</span></span><br/> | <span data-ttu-id="10ada-430">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10ada-430">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10ada-431">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10ada-431">Namespace</span></span><br/>                | <span data-ttu-id="10ada-432">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="10ada-432">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10ada-433">MOF</span><span class="sxs-lookup"><span data-stu-id="10ada-433">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ada-434"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10ada-434"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ada-435">DLL</span><span class="sxs-lookup"><span data-stu-id="10ada-435">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ada-436"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10ada-436"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ada-437">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10ada-437">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ada-438">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="10ada-438">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="10ada-439">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="10ada-439">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
