---
description: Rappresenta il punto di connessione logico per una scheda di rete. Quando l'endpoint del Wi-Fi è connesso a una porta di commutazione, la scheda di rete connessa all'endpoint Wi-Fi dispone di connettività di rete.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Classe Msvm_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966641"
---
# <a name="msvm_wifiendpoint-class"></a><span data-ttu-id="f6264-104">\_Classe MSVM WiFiEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6264-104">Msvm\_WiFiEndpoint class</span></span>

<span data-ttu-id="f6264-105">Rappresenta il punto di connessione logico per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f6264-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="f6264-106">Quando l'endpoint del Wi-Fi è connesso a una porta di commutazione, la scheda di rete connessa all'endpoint Wi-Fi dispone di connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="f6264-106">When the Wi-Fi endpoint is connected to a switch port, the network adapter connected to the Wi-Fi endpoint has network connectivity.</span></span>

<span data-ttu-id="f6264-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f6264-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6264-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6264-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a><span data-ttu-id="f6264-109">Members</span><span class="sxs-lookup"><span data-stu-id="f6264-109">Members</span></span>

<span data-ttu-id="f6264-110">La **classe \_ WiFiEndpoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6264-110">The **Msvm\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="f6264-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6264-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6264-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6264-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6264-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6264-113">Methods</span></span>

<span data-ttu-id="f6264-114">La **classe \_ WiFiEndpoint di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f6264-114">The **Msvm\_WiFiEndpoint** class has these methods.</span></span>



| <span data-ttu-id="f6264-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="f6264-115">Method</span></span>                 | <span data-ttu-id="f6264-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6264-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="f6264-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f6264-117">**RequestStateChange**</span></span> | <span data-ttu-id="f6264-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f6264-118">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f6264-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6264-119">Properties</span></span>

<span data-ttu-id="f6264-120">La **classe \_ WiFiEndpoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6264-120">The **Msvm\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6264-121">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="f6264-121">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-124">Contiene l'indirizzo MAC del punto di accesso a cui è attualmente associato l'endpoint Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f6264-124">Contains the MAC address of the access point with which the Wi-Fi endpoint is currently associated.</span></span> <span data-ttu-id="f6264-125">Se l'endpoint Wi-Fi non è attualmente associato, **AccessPointAddress** deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="f6264-125">If the Wi-Fi endpoint is not currently associated, then **AccessPointAddress** should be **Null**.</span></span> <span data-ttu-id="f6264-126">L'indirizzo MAC deve essere formattato come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC nell'ordine dei bit canonico (ad esempio, il bit dell'indirizzo del gruppo viene trovato nel bit di ordine inferiore del primo carattere della stringa).</span><span class="sxs-lookup"><span data-stu-id="f6264-126">The MAC address should be formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (for example, the Group address bit is found in the low order bit of the first character of the string).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-127">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="f6264-127">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-128">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f6264-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6264-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-130">Altri indirizzi unicast che possono essere utilizzati per comunicare con l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="f6264-130">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="f6264-131">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-131">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-132">**Associazione**</span><span class="sxs-lookup"><span data-stu-id="f6264-132">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f6264-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-135">Indica se l'endpoint Wi-Fi è attualmente associato a un punto di accesso o a una stazione client.</span><span class="sxs-lookup"><span data-stu-id="f6264-135">Indicates whether the Wi-Fi endpoint is currently associated to an access point or client station.</span></span>

<span data-ttu-id="f6264-136">Contiene **true** se l'endpoint Wi-Fi è associato a un punto di accesso o a una stazione client; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f6264-136">Contains **True** if the Wi-Fi endpoint is associated to an access point or client station; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f6264-137">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="f6264-137">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-138">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-140">Specifica il metodo usato per autenticare l'endpoint Wi-Fi e la rete tra loro.</span><span class="sxs-lookup"><span data-stu-id="f6264-140">Specifies the method used to authenticate the Wi-Fi endpoint and the network to one another.</span></span>

<dl> <dt>

<span data-ttu-id="f6264-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f6264-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6264-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Apri sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="f6264-143"><span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Chiave condivisa** (3)</span><span class="sxs-lookup"><span data-stu-id="f6264-144"><span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Shared Key** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**PSK wpa** (4)</span><span class="sxs-lookup"><span data-stu-id="f6264-145"><span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="f6264-146"><span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="f6264-147"><span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="f6264-148"><span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="f6264-149"><span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (9..</span><span class="sxs-lookup"><span data-stu-id="f6264-150"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (9..</span></span> <span data-ttu-id="f6264-151">)</span><span class="sxs-lookup"><span data-stu-id="f6264-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="f6264-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-153">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6264-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-155">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="f6264-155">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="f6264-156">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-156">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="f6264-157">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="f6264-157">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="f6264-158">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="f6264-158">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="f6264-159">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="f6264-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="f6264-160"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f6264-161"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="f6264-162"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="f6264-163"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="f6264-164"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="f6264-165"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="f6264-166"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="f6264-167"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="f6264-168"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="f6264-169"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="f6264-170">)</span><span class="sxs-lookup"><span data-stu-id="f6264-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-171">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="f6264-171">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-174">Indica il tipo di base del set di servizi (BSS) della rete che corrisponde all'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f6264-174">Indicates the Basic Service Set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="f6264-175">Un set di servizi di base è un set di stazioni controllate da una singola funzione di coordinamento.</span><span class="sxs-lookup"><span data-stu-id="f6264-175">A Basic Service Set is a set of stations controlled by a single coordination function.</span></span>



| <span data-ttu-id="f6264-176">Valore</span><span class="sxs-lookup"><span data-stu-id="f6264-176">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="f6264-177">Significato</span><span class="sxs-lookup"><span data-stu-id="f6264-177">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="f6264-178"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-178"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <span data-ttu-id="f6264-179"><dt>**Indipendente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-179"><dt>**Independent**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="f6264-180">L'endpoint Wi-Fi è associato direttamente a un'altra stazione client.</span><span class="sxs-lookup"><span data-stu-id="f6264-180">The Wi-Fi endpoint is associated directly to another client station.</span></span><br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <span data-ttu-id="f6264-181"><dt>**Infrastruttura**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-181"><dt>**Infrastructure**</dt> <dt>3</dt></span></span> </dl>    | <span data-ttu-id="f6264-182">L'endpoint Wi-Fi è associato a una rete tramite un punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="f6264-182">The Wi-Fi endpoint is associated to a network by using an access point.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="f6264-183"><dt> **DMTF riservato**</dt> <dt>4..</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-183"><dt>**DMTF Reserved** </dt> <dt>4.. </dt></span></span> </dl> |                                                                                    |



 

</dd> <dt>

<span data-ttu-id="f6264-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f6264-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-187">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6264-187">A short description of the object.</span></span> <span data-ttu-id="f6264-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f6264-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-192">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="f6264-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f6264-193">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f6264-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6264-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-195">**Connessione effettuata**</span><span class="sxs-lookup"><span data-stu-id="f6264-195">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f6264-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-198">Questa proprietà è impostata su **true** se l'endpoint Wi-Fi è connesso a una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="f6264-198">This property is set to **True** if the Wi-Fi endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="f6264-199">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6264-199">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-200">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-202">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6264-202">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f6264-203">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f6264-203">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f6264-204">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-204">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-205">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f6264-205">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-208">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="f6264-208">A description of the object.</span></span> <span data-ttu-id="f6264-209">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-210">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f6264-210">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-213">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="f6264-213">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f6264-214">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f6264-214">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6264-215">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f6264-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-219">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6264-219">A display name for the object.</span></span> <span data-ttu-id="f6264-220">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="f6264-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-222">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-224">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f6264-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="f6264-225">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6264-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f6264-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="f6264-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="f6264-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="f6264-228"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-229">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="f6264-229">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-230">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-232">Specifica lo stato abilitato del sistema pianificato.</span><span class="sxs-lookup"><span data-stu-id="f6264-232">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="f6264-233">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6264-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="f6264-234">Valore</span><span class="sxs-lookup"><span data-stu-id="f6264-234">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="f6264-235">Significato</span><span class="sxs-lookup"><span data-stu-id="f6264-235">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="f6264-236"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-236"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="f6264-237">Il sistema è disattivato.</span><span class="sxs-lookup"><span data-stu-id="f6264-237">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="f6264-238"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-238"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="f6264-239">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="f6264-239">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="f6264-240"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-240"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="f6264-241">Il sistema è abilitato, ma non è in linea.</span><span class="sxs-lookup"><span data-stu-id="f6264-241">The system is enabled, but offline.</span></span> <span data-ttu-id="f6264-242">Tutte le nuove richieste verranno eliminate.</span><span class="sxs-lookup"><span data-stu-id="f6264-242">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6264-243">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f6264-243">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-246">Specifica il metodo di crittografia utilizzato per proteggere la riservatezza dei dati inviati e ricevuti dall'endpoint Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="f6264-246">Specifies the encryption method in use to protect the confidentiality of data sent and received by the Wi-Fi endpoint.</span></span>

<dl> <dt>

<span data-ttu-id="f6264-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f6264-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6264-248"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="f6264-249"><span id="WEP"></span><span id="wep"></span>**WEP** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="f6264-250"><span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="f6264-251"><span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (5)</span><span class="sxs-lookup"><span data-stu-id="f6264-252"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (6..</span><span class="sxs-lookup"><span data-stu-id="f6264-253"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (6..</span></span> <span data-ttu-id="f6264-254">)</span><span class="sxs-lookup"><span data-stu-id="f6264-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-255">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="f6264-255">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-256">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f6264-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6264-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-258">Indirizzi multicast su cui è in ascolto l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="f6264-258">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="f6264-259">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-259">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-260">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f6264-260">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-261">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-263">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f6264-263">The current health of the element.</span></span> <span data-ttu-id="f6264-264">Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f6264-264">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f6264-265">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="f6264-265">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f6264-266">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-267">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="f6264-267">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-268">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-270">Contiene il tipo EAP (Extensible Authentication Protocol) se e solo se **AuthenticationMethod** contiene 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) o 8 (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="f6264-270">Contains the Extensible Authentication Protocol (EAP) type if and only if **AuthenticationMethod** contains 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x), or 8 (CCKM IEEE 802.1x).</span></span>

<dl> <dt>

<span data-ttu-id="f6264-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="f6264-271"><span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="f6264-272"><span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="f6264-273"><span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="f6264-274"><span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="f6264-275"><span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="f6264-276"><span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="f6264-277"><span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="f6264-278"><span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="f6264-279"><span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="f6264-280"><span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="f6264-281"><span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (11..</span><span class="sxs-lookup"><span data-stu-id="f6264-282"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (11..</span></span> <span data-ttu-id="f6264-283">)</span><span class="sxs-lookup"><span data-stu-id="f6264-283">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-284">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6264-284">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-285">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6264-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-287">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f6264-287">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f6264-288">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-289">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6264-289">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-292">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="f6264-292">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6264-293">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f6264-293">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f6264-294">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-294">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-295">**LANId**</span><span class="sxs-lookup"><span data-stu-id="f6264-295">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-298">Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f6264-298">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="f6264-299">Se l'endpoint non è attualmente attivo/connesso o queste informazioni non sono note, questa proprietà sarà **null**.</span><span class="sxs-lookup"><span data-stu-id="f6264-299">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="f6264-300">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-300">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-301">**LANType**</span><span class="sxs-lookup"><span data-stu-id="f6264-301">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-302">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-304">Questa proprietà è deprecata al posto della proprietà **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="f6264-304">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="f6264-305">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-305">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-306">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="f6264-306">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-309">Qualificatori: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="f6264-309">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="f6264-310">Indirizzo MAC utilizzato per la comunicazione con l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="f6264-310">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="f6264-311">L'indirizzo MAC è formattato come dodici cifre esadecimali (ad esempio, "010203040506"), ciascuna delle quali rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico in base a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="f6264-311">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="f6264-312">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-312">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-313">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="f6264-313">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-314">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6264-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-316">Qualificatori: **unità** ("bits")</span><span class="sxs-lookup"><span data-stu-id="f6264-316">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="f6264-317">Dimensione massima, in numero di bit, del campo informazioni che può essere inviato o ricevuto dall'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="f6264-317">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="f6264-318">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-318">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-319">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f6264-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-320">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-322">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="f6264-322">The label by which the object is known.</span></span> <span data-ttu-id="f6264-323">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-324">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="f6264-324">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-327">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6264-327">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f6264-328">Contiene l'euristica di denominazione selezionata per garantire che il valore della proprietà **Name** sia univoco.</span><span class="sxs-lookup"><span data-stu-id="f6264-328">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="f6264-329">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-329">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-330">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f6264-330">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-333">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f6264-333">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f6264-334">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f6264-334">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6264-335">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-335">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f6264-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-337">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6264-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-339">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6264-339">The current statuses of the object.</span></span> <span data-ttu-id="f6264-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-341">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="f6264-341">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-344">Specifica il metodo di autenticazione 802,11 se e solo se **AuthenticationMethod** contiene 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f6264-344">Specifies the 802.11 authentication method if and only if **AuthenticationMethod** contains 1 (Other).</span></span> <span data-ttu-id="f6264-345">Il formato di questa stringa è specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="f6264-345">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="f6264-346">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="f6264-346">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-349">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="f6264-349">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="f6264-350">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f6264-350">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="f6264-351">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-351">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-352">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="f6264-352">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-355">Specifica il metodo di crittografia 802,11 se e solo se **EncryptionMethod** contiene 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f6264-355">Specifies the 802.11 encryption method if and only if **EncryptionMethod** contains 1 (Other).</span></span> <span data-ttu-id="f6264-356">Il formato di questa stringa è specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="f6264-356">The format of this string is vendor specific.</span></span>

</dd> <dt>

<span data-ttu-id="f6264-357">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="f6264-357">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-358">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-360">Questa proprietà è deprecata al posto della proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="f6264-360">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="f6264-361">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-361">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-362">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="f6264-362">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-365">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="f6264-365">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="f6264-366">Stringa che descrive il tipo di endpoint del protocollo quando la proprietà **ProtocolIFType** di questa classe (o una delle relative sottoclassi) viene impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="f6264-366">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="f6264-367">Questa proprietà deve essere impostata su **null** se la proprietà **ProtocolIFType** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="f6264-367">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="f6264-368">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-368">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-369">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f6264-369">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-370">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-372">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="f6264-372">Provides high level status information.</span></span> <span data-ttu-id="f6264-373">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="f6264-373">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="f6264-374">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="f6264-374">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f6264-375">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-376">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="f6264-376">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-377">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-378">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-379">La proprietà viene utilizzata per suddividere in categorie e classificare le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f6264-379">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="f6264-380">Se **ProtocolIFType** è impostato su 1 (other), le informazioni sul tipo devono essere fornite nella proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="f6264-380">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="f6264-381">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-381">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="f6264-382">**ProtocolIFType** è un'enumerazione sincronizzata con [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="f6264-382">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="f6264-383">Sono inclusi anche valori aggiuntivi definiti da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f6264-383">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="f6264-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6264-384"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="f6264-385"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA riservato** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="f6264-386"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f6264-387"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (4301..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f6264-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768..</span><span class="sxs-lookup"><span data-stu-id="f6264-388"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="f6264-389">)</span><span class="sxs-lookup"><span data-stu-id="f6264-389">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6264-390">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="f6264-390">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-391">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-393">Questa proprietà è deprecata al posto della proprietà **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="f6264-393">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="f6264-394">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-394">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="f6264-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-396">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-398">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="f6264-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="f6264-399">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-400">**Status**</span><span class="sxs-lookup"><span data-stu-id="f6264-400">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-403">Descrive lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f6264-403">Describes the status of the element.</span></span> <span data-ttu-id="f6264-404">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-404">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="f6264-405">OK</span><span class="sxs-lookup"><span data-stu-id="f6264-405">"OK"</span></span>

<span data-ttu-id="f6264-406">Errore</span><span class="sxs-lookup"><span data-stu-id="f6264-406">"Error"</span></span>

<span data-ttu-id="f6264-407">Degradato</span><span class="sxs-lookup"><span data-stu-id="f6264-407">"Degraded"</span></span>

<span data-ttu-id="f6264-408">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f6264-408">"Unknown"</span></span>

<span data-ttu-id="f6264-409">"Errore di predazione"</span><span class="sxs-lookup"><span data-stu-id="f6264-409">"Pred Fail"</span></span>

<span data-ttu-id="f6264-410">Avvio</span><span class="sxs-lookup"><span data-stu-id="f6264-410">"Starting"</span></span>

<span data-ttu-id="f6264-411">Arresto</span><span class="sxs-lookup"><span data-stu-id="f6264-411">"Stopping"</span></span>

<span data-ttu-id="f6264-412">Servizio</span><span class="sxs-lookup"><span data-stu-id="f6264-412">"Service"</span></span>

<span data-ttu-id="f6264-413">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="f6264-413">"Stressed"</span></span>

<span data-ttu-id="f6264-414">"Non ripristino"</span><span class="sxs-lookup"><span data-stu-id="f6264-414">"NonRecover"</span></span>

<span data-ttu-id="f6264-415">"Nessun contatto"</span><span class="sxs-lookup"><span data-stu-id="f6264-415">"No Contact"</span></span>

<span data-ttu-id="f6264-416">"Lost comm"</span><span class="sxs-lookup"><span data-stu-id="f6264-416">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="f6264-417">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f6264-417">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-418">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f6264-418">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6264-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-420">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f6264-420">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f6264-421">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f6264-421">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-422">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6264-422">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-423">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-425">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="f6264-425">The hosting system's creation class name.</span></span> <span data-ttu-id="f6264-426">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-426">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-427">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f6264-427">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f6264-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6264-430">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="f6264-430">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="f6264-431">Nome del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="f6264-431">The name of the hosting system.</span></span> <span data-ttu-id="f6264-432">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="f6264-432">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-433">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f6264-433">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-434">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6264-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-436">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f6264-436">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="f6264-437">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-437">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6264-438">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="f6264-438">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6264-439">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6264-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6264-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6264-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6264-441">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f6264-441">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="f6264-442">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6264-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6264-443">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6264-443">Requirements</span></span>



| <span data-ttu-id="f6264-444">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6264-444">Requirement</span></span> | <span data-ttu-id="f6264-445">Valore</span><span class="sxs-lookup"><span data-stu-id="f6264-445">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6264-446">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6264-446">Minimum supported client</span></span><br/> | <span data-ttu-id="f6264-447">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6264-447">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6264-448">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6264-448">Minimum supported server</span></span><br/> | <span data-ttu-id="f6264-449">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6264-449">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6264-450">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f6264-450">Namespace</span></span><br/>                | <span data-ttu-id="f6264-451">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f6264-451">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6264-452">MOF</span><span class="sxs-lookup"><span data-stu-id="f6264-452">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6264-453"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-453"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6264-454">DLL</span><span class="sxs-lookup"><span data-stu-id="f6264-454">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6264-455"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6264-455"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

