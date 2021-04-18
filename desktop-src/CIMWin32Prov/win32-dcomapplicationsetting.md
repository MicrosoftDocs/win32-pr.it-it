---
description: Win32 \_ DCOMApplicationSetting&\# 8194; Classe WMI che rappresenta le impostazioni di un'applicazione DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305274"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="95237-103">Win32 \_ DCOMApplicationSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="95237-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="95237-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DCOMApplicationSetting Win32** rappresenta le impostazioni di un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="95237-105">Contiene le opzioni di configurazione DCOM associate alla chiave **AppID** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="95237-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="95237-106">Queste opzioni sono valide per i componenti raggruppati logicamente sotto la classe dell'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="95237-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="95237-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="95237-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="95237-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="95237-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95237-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95237-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="95237-110">Members</span><span class="sxs-lookup"><span data-stu-id="95237-110">Members</span></span>

<span data-ttu-id="95237-111">La classe **Win32 \_ DCOMApplicationSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="95237-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="95237-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="95237-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="95237-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="95237-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95237-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="95237-114">Methods</span></span>

<span data-ttu-id="95237-115">La classe **Win32 \_ DCOMApplicationSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="95237-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="95237-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="95237-116">Method</span></span>                                                                                                                        | <span data-ttu-id="95237-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95237-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95237-118">**GetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="95237-119">Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati ad accedere a un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="95237-120">**GetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="95237-121">Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati a configurare un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="95237-122">**GetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="95237-123">Ottiene il descrittore di sicurezza che controlla gli utenti autorizzati ad avviare un'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="95237-124">**SetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="95237-125">Aggiorna il descrittore di sicurezza di accesso dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="95237-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="95237-126">**SetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="95237-127">Aggiorna il descrittore di sicurezza della configurazione dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="95237-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="95237-128">**SetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="95237-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="95237-129">Aggiorna il descrittore di sicurezza di avvio dell'applicazione DCOM con un nuovo descrittore di sicurezza definito da un'istanza della classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="95237-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="95237-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="95237-130">Properties</span></span>

<span data-ttu-id="95237-131">La classe **Win32 \_ DCOMApplicationSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="95237-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95237-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="95237-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-135">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-136">Identificatore univoco globale (GUID) per l'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="95237-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="95237-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95237-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95237-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="95237-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="95237-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-141">Livello di autenticazione client minimo richiesto da questo server COM.</span><span class="sxs-lookup"><span data-stu-id="95237-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="95237-142">Se **null**, vengono utilizzati i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="95237-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="95237-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (1)</span><span class="sxs-lookup"><span data-stu-id="95237-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="95237-144">Nessuno (nessuna autenticazione eseguita)</span><span class="sxs-lookup"><span data-stu-id="95237-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="95237-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connetti** (2)</span><span class="sxs-lookup"><span data-stu-id="95237-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="95237-146">Connetti (l'autenticazione viene eseguita solo quando il client stabilisce una relazione con l'applicazione)</span><span class="sxs-lookup"><span data-stu-id="95237-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="95237-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Chiamata** (3)</span><span class="sxs-lookup"><span data-stu-id="95237-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="95237-148">Call (l'autenticazione viene eseguita solo all'inizio di ogni chiamata quando l'applicazione riceve la richiesta)</span><span class="sxs-lookup"><span data-stu-id="95237-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="95237-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Pacchetto** (4)</span><span class="sxs-lookup"><span data-stu-id="95237-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="95237-150">Pacchetto (l'autenticazione viene eseguita su tutti i dati ricevuti dal client)</span><span class="sxs-lookup"><span data-stu-id="95237-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="95237-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span><span class="sxs-lookup"><span data-stu-id="95237-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="95237-152">PacketIntegrity (tutti i dati trasferiti tra il client e l'applicazione vengono autenticati e verificati)</span><span class="sxs-lookup"><span data-stu-id="95237-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="95237-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span><span class="sxs-lookup"><span data-stu-id="95237-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="95237-154">PacketPrivacy (vengono usate le proprietà degli altri livelli di autenticazione e tutti i dati sono crittografati)</span><span class="sxs-lookup"><span data-stu-id="95237-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95237-155">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="95237-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-158">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95237-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95237-159">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="95237-159">Short textual description of the current object.</span></span>

<span data-ttu-id="95237-160">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="95237-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="95237-161">**CustomSurrogate**</span><span class="sxs-lookup"><span data-stu-id="95237-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-164">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-165">Nome del surrogato personalizzato in cui è attivata l'applicazione DCOM in-process.</span><span class="sxs-lookup"><span data-stu-id="95237-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="95237-166">Se questo valore è **null** e la chiave **UseSurrogate** è **true**, il sistema fornisce un processo surrogato.</span><span class="sxs-lookup"><span data-stu-id="95237-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="95237-167">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="95237-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95237-170">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="95237-170">Textual description of the current object.</span></span>

<span data-ttu-id="95237-171">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="95237-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="95237-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="95237-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-173">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95237-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95237-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-175">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-176">L'applicazione DCOM recupera lo stato salvato dell'applicazione o inizia dallo stato in cui l'applicazione viene inizializzata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="95237-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="95237-177">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="95237-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-180">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-181">Nome dei servizi forniti dall'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="95237-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="95237-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="95237-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="95237-185">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-186">Nome del server remoto in cui è attivata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="95237-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="95237-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="95237-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-190">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ RunAs \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-191">Account utente specifico con cui l'applicazione deve essere eseguita all'attivazione.</span><span class="sxs-lookup"><span data-stu-id="95237-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="95237-192">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="95237-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-195">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-196">Parametri della riga di comando passati all'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="95237-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="95237-197">Questa operazione è valida solo se l'applicazione viene scritta come servizio basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="95237-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="95237-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="95237-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="95237-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95237-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="95237-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95237-201">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="95237-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="95237-202">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="95237-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="95237-203">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="95237-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="95237-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="95237-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95237-205">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="95237-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95237-206">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="95237-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="95237-207">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ Local \_ Machine \\ \\ software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="95237-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="95237-208">L'applicazione DCOM può essere attivata come server out-of-process usando un file eseguibile surrogato.</span><span class="sxs-lookup"><span data-stu-id="95237-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95237-209">Commenti</span><span class="sxs-lookup"><span data-stu-id="95237-209">Remarks</span></span>

<span data-ttu-id="95237-210">La classe **Win32 \_ DCOMApplicationSetting** è derivata dalla [**\_ comimpostazione Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="95237-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95237-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95237-211">Requirements</span></span>



| <span data-ttu-id="95237-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="95237-212">Requirement</span></span> | <span data-ttu-id="95237-213">Valore</span><span class="sxs-lookup"><span data-stu-id="95237-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95237-214">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95237-214">Minimum supported client</span></span><br/> | <span data-ttu-id="95237-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95237-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95237-216">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95237-216">Minimum supported server</span></span><br/> | <span data-ttu-id="95237-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95237-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95237-218">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95237-218">Namespace</span></span><br/>                | <span data-ttu-id="95237-219">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="95237-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95237-220">MOF</span><span class="sxs-lookup"><span data-stu-id="95237-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95237-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95237-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95237-222">DLL</span><span class="sxs-lookup"><span data-stu-id="95237-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95237-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95237-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95237-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95237-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95237-225">**Comimpostazioni Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="95237-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="95237-226">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95237-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="95237-227">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="95237-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="95237-228">Oggetti descrittore di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="95237-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="95237-229">Modifica della sicurezza di accesso per gli oggetti a protezione diretta</span><span class="sxs-lookup"><span data-stu-id="95237-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

