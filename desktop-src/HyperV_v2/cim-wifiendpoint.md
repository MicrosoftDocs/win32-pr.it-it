---
description: Rappresenta un endpoint di comunicazione wireless, che può inviare e ricevere frame di dati quando il dispositivo di interfaccia associato è connesso con una LAN wireless IEEE 802,11.
ms.assetid: 61743402-f333-4501-ba17-e676d85f72f3
title: Classe CIM_WiFiEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiEndpoint
- CIM_WiFiEndpoint.LANID
- CIM_WiFiEndpoint.ProtocolIFType
- CIM_WiFiEndpoint.EncryptionMethod
- CIM_WiFiEndpoint.OtherEncryptionMethod
- CIM_WiFiEndpoint.AuthenticationMethod
- CIM_WiFiEndpoint.OtherAuthenticationMethod
- CIM_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- CIM_WiFiEndpoint.AccessPointAddress
- CIM_WiFiEndpoint.BSSType
- CIM_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e09d040f9d4530bee4347528d704cfe2e9403b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315920"
---
# <a name="cim_wifiendpoint-class"></a><span data-ttu-id="0ad84-103">CIM \_ WiFiEndpoint (classe)</span><span class="sxs-lookup"><span data-stu-id="0ad84-103">CIM\_WiFiEndpoint class</span></span>

<span data-ttu-id="0ad84-104">Rappresenta un endpoint di comunicazione wireless, che può inviare e ricevere frame di dati quando il dispositivo di interfaccia associato è connesso con una LAN wireless IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="0ad84-104">Represents a wireless communication endpoint, which can send and receive data frames when its associated interface device is connected with an IEEE 802.11 wireless LAN.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ad84-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Network::Wireless"), AMENDMENT]
class CIM_WiFiEndpoint : CIM_LANEndpoint
{
  string  LANID;
  uint16  ProtocolIFType = 71;
  uint16  EncryptionMethod;
  string  OtherEncryptionMethod;
  uint16  AuthenticationMethod;
  string  OtherAuthenticationMethod;
  uint16  IEEE8021xAuthenticationProtocol;
  string  AccessPointAddress;
  uint16  BSSType;
  boolean Associated;
};
```

## <a name="members"></a><span data-ttu-id="0ad84-106">Members</span><span class="sxs-lookup"><span data-stu-id="0ad84-106">Members</span></span>

<span data-ttu-id="0ad84-107">La classe **CIM \_ WiFiEndpoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ad84-107">The **CIM\_WiFiEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="0ad84-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ad84-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ad84-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ad84-109">Properties</span></span>

<span data-ttu-id="0ad84-110">La classe **CIM \_ WiFiEndpoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ad84-110">The **CIM\_WiFiEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ad84-111">**AccessPointAddress**</span><span class="sxs-lookup"><span data-stu-id="0ad84-111">**AccessPointAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ad84-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-114">Indirizzo MAC del punto di accesso associato all'endpoint Wi-Fi; in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="0ad84-114">The MAC address of the access point that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ad84-115">**Associazione**</span><span class="sxs-lookup"><span data-stu-id="0ad84-115">**Associated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0ad84-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-118">**true** se l'endpoint WiFi è attualmente associato a un punto di accesso o a una stazione client; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0ad84-118">**true** if the WiFi endpoint is currently associated with an access point or client station; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0ad84-119">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="0ad84-119">**AuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-120">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad84-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-122">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**","**CIM \_ WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**","**CIM \_ WiFiEndpoint**.**OtherAuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="0ad84-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**", "**CIM\_WiFiEndpoint**.**IEEE8021xAuthenticationProtocol**", "**CIM\_WiFiEndpoint**.**OtherAuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-123">Tipo di autenticazione usato tra l'endpoint Wi-Fi e la rete.</span><span class="sxs-lookup"><span data-stu-id="0ad84-123">The authentication type used between the Wi-Fi endpoint and the network.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ad84-124">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ad84-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ad84-125">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0ad84-125">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>

<span data-ttu-id="0ad84-126">**Apri sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="0ad84-126">**Open System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>

<span data-ttu-id="0ad84-127">**Chiave condivisa** (3)</span><span class="sxs-lookup"><span data-stu-id="0ad84-127">**Shared Key** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>

<span data-ttu-id="0ad84-128">**PSK wpa** (4)</span><span class="sxs-lookup"><span data-stu-id="0ad84-128">**WPA PSK** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>

<span data-ttu-id="0ad84-129">**WPA IEEE 802.1 x** (5)</span><span class="sxs-lookup"><span data-stu-id="0ad84-129">**WPA IEEE 802.1x** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>

<span data-ttu-id="0ad84-130">**WPA2 PSK** (6)</span><span class="sxs-lookup"><span data-stu-id="0ad84-130">**WPA2 PSK** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>

<span data-ttu-id="0ad84-131">**WPA2 IEEE 802.1 x** (7)</span><span class="sxs-lookup"><span data-stu-id="0ad84-131">**WPA2 IEEE 802.1x** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>

<span data-ttu-id="0ad84-132">**CCKM IEEE 802.1 x** (8)</span><span class="sxs-lookup"><span data-stu-id="0ad84-132">**CCKM IEEE 802.1x** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ad84-133">**DMTF riservato** (9...)</span><span class="sxs-lookup"><span data-stu-id="0ad84-133">**DMTF Reserved** (9..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ad84-134">**BSSType**</span><span class="sxs-lookup"><span data-stu-id="0ad84-134">**BSSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad84-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-137">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3,16")</span><span class="sxs-lookup"><span data-stu-id="0ad84-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 3.16")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-138">Tipo di base del set di servizi (BSS) della rete che corrisponde all'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0ad84-138">The basic service set (BSS) type of the network that corresponds to the instance.</span></span> <span data-ttu-id="0ad84-139">Un BSS è un set di stazioni controllate da una singola funzione di coordinamento.</span><span class="sxs-lookup"><span data-stu-id="0ad84-139">A BSS is a set of stations controlled by a single coordination function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ad84-140">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ad84-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="0ad84-141">**Indipendente** (2)</span><span class="sxs-lookup"><span data-stu-id="0ad84-141">**Independent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span>

<span data-ttu-id="0ad84-142">**Infrastruttura** (3)</span><span class="sxs-lookup"><span data-stu-id="0ad84-142">**Infrastructure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ad84-143">**DMTF riservato** (4..)</span><span class="sxs-lookup"><span data-stu-id="0ad84-143">**DMTF Reserved** (4..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ad84-144">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="0ad84-144">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad84-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**","**CIM \_ WiFiEndpoint**.**OtherEncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="0ad84-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**", "**CIM\_WiFiEndpoint**.**OtherEncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-148">Tipo di crittografia utilizzato per l'invio e la ricezione di dati tramite l'endpoint Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="0ad84-148">The encryption type used when sending and receiving data through the Wi-Fi endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0ad84-149">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0ad84-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ad84-150">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0ad84-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WEP"></span><span id="wep"></span>

<span data-ttu-id="0ad84-151">**WEP** (2)</span><span class="sxs-lookup"><span data-stu-id="0ad84-151">**WEP** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TKIP"></span><span id="tkip"></span>

<span data-ttu-id="0ad84-152">**TKIP** (3)</span><span class="sxs-lookup"><span data-stu-id="0ad84-152">**TKIP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CCMP"></span><span id="ccmp"></span>

<span data-ttu-id="0ad84-153">**CCMP** (4)</span><span class="sxs-lookup"><span data-stu-id="0ad84-153">**CCMP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0ad84-154">**Nessuno** (5)</span><span class="sxs-lookup"><span data-stu-id="0ad84-154">**None** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ad84-155">**DMTF riservato** (6...)</span><span class="sxs-lookup"><span data-stu-id="0ad84-155">**DMTF Reserved** (6..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ad84-156">**IEEE8021xAuthenticationProtocol**</span><span class="sxs-lookup"><span data-stu-id="0ad84-156">**IEEE8021xAuthenticationProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad84-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-159">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017. IETF "," RFC2716. IETF "," draft-ietf-pppext-EAP-TTLS. IETF "," Draft-Kamath-pppext-PEAPv0. IETF "," Draft-Josefsson-pppext-EAP-TLS-EAP "," RFC4851. IETF "," RFC3748. IETF "," RFC4764. IETF "," RFC4186. IETF "," RFC4187. IETF "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="0ad84-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RFC4017.IETF", "RFC2716.IETF", "draft-ietf-pppext-eap-ttls.IETF", "draft-kamath-pppext-peapv0.IETF", "draft-josefsson-pppext-eap-tls-eap", "RFC4851.IETF", "RFC3748.IETF", "RFC4764.IETF", "RFC4186.IETF", "RFC4187.IETF"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-160">Il tipo EAP (Extensible Authentication Protocol) per l'endpoint Wi-Fi quando **AuthenticationMethod** contiene "7" (WPA IEEE 802.1 x) o "8" (CCKM IEEE 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="0ad84-160">The EAP (Extensible Authentication Protocol) type for the Wi-Fi endpoint when **AuthenticationMethod** contains "7" (WPA IEEE 802.1x) or "8" (CCKM IEEE 802.1x).</span></span>

<dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>

<span data-ttu-id="0ad84-161">**EAP-TLS** (0)</span><span class="sxs-lookup"><span data-stu-id="0ad84-161">**EAP-TLS** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>

<span data-ttu-id="0ad84-162">**EAP-TTLS/MSCHAPv2** (1)</span><span class="sxs-lookup"><span data-stu-id="0ad84-162">**EAP-TTLS/MSCHAPv2** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>

<span data-ttu-id="0ad84-163">**PEAPv0/EAP-MSCHAPv2** (2)</span><span class="sxs-lookup"><span data-stu-id="0ad84-163">**PEAPv0/EAP-MSCHAPv2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>

<span data-ttu-id="0ad84-164">**PEAPv1/EAP-GTC** (3)</span><span class="sxs-lookup"><span data-stu-id="0ad84-164">**PEAPv1/EAP-GTC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>

<span data-ttu-id="0ad84-165">**EAP-FAST/MSCHAPv2** (4)</span><span class="sxs-lookup"><span data-stu-id="0ad84-165">**EAP-FAST/MSCHAPv2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>

<span data-ttu-id="0ad84-166">**EAP-FAST/GTC** (5)</span><span class="sxs-lookup"><span data-stu-id="0ad84-166">**EAP-FAST/GTC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>

<span data-ttu-id="0ad84-167">**EAP-MD5** (6)</span><span class="sxs-lookup"><span data-stu-id="0ad84-167">**EAP-MD5** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>

<span data-ttu-id="0ad84-168">**EAP-PSK** (7)</span><span class="sxs-lookup"><span data-stu-id="0ad84-168">**EAP-PSK** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>

<span data-ttu-id="0ad84-169">**EAP-SIM** (8)</span><span class="sxs-lookup"><span data-stu-id="0ad84-169">**EAP-SIM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>

<span data-ttu-id="0ad84-170">**EAP-AKA** (9)</span><span class="sxs-lookup"><span data-stu-id="0ad84-170">**EAP-AKA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>

<span data-ttu-id="0ad84-171">**EAP-FAST/TLS** (10)</span><span class="sxs-lookup"><span data-stu-id="0ad84-171">**EAP-FAST/TLS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ad84-172">**DMTF riservato** (11..)</span><span class="sxs-lookup"><span data-stu-id="0ad84-172">**DMTF Reserved** (11..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0ad84-173">**LANId**</span><span class="sxs-lookup"><span data-stu-id="0ad84-173">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ad84-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-176">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LanID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span><span class="sxs-lookup"><span data-stu-id="0ad84-176">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LANID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("IEEE 802.11-2007 \| 7.3.2.1")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-177">Identificatore del set di servizi (SSID) della LAN wireless associata all'endpoint Wi-Fi; in caso contrario, **null**.</span><span class="sxs-lookup"><span data-stu-id="0ad84-177">The service set identifier (SSID) of the wireless LAN that is associated with the Wi-Fi endpoint; otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ad84-178">**OtherAuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="0ad84-178">**OtherAuthenticationMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ad84-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-181">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**AuthenticationMethod**")</span><span class="sxs-lookup"><span data-stu-id="0ad84-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**AuthenticationMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-182">Tipo di autenticazione usato tra l'endpoint Wi-Fi e la rete quando **AuthenticationMethod** contiene "1" (other).</span><span class="sxs-lookup"><span data-stu-id="0ad84-182">The authentication type used between the Wi-Fi endpoint and the network when **AuthenticationMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0ad84-183">**OtherEncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="0ad84-183">**OtherEncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ad84-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-186">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ WiFiEndpoint**.**EncryptionMethod**")</span><span class="sxs-lookup"><span data-stu-id="0ad84-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_WiFiEndpoint**.**EncryptionMethod**")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-187">Descrive il tipo di crittografia per l'endpoint Wi-Fi quando **EncryptionMethod** contiene "1" (other).</span><span class="sxs-lookup"><span data-stu-id="0ad84-187">Describes the encryption type for the Wi-Fi endpoint when **EncryptionMethod** contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0ad84-188">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="0ad84-188">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad84-189">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0ad84-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ad84-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad84-191">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span><span class="sxs-lookup"><span data-stu-id="0ad84-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ProtocolIFType")</span></span>
</dt> </dl>

<span data-ttu-id="0ad84-192">Categoria o classificazione di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="0ad84-192">The category or classification of this instance.</span></span> <span data-ttu-id="0ad84-193">I valori possibili sono limitati ai Wi-Fi e ai valori riservati DMTF e [IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="0ad84-193">The possible values are limited to the Wi-Fi and reserved values from the DMTF and [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span>

<span data-ttu-id="0ad84-194">Se **ProtocolIFType** è impostato su "1" (other), le informazioni sul tipo devono essere fornite nella proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="0ad84-194">If the **ProtocolIFType** is set to "1" (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0ad84-195">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0ad84-195">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

<span data-ttu-id="0ad84-196">**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="0ad84-196">**IEEE 802.11** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

<span data-ttu-id="0ad84-197">**IANA riservato** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="0ad84-197">**IANA Reserved** (225..4095)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0ad84-198">**DMTF riservato** (4301.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0ad84-198">**DMTF Reserved** (4301..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0ad84-199">**Fornitore riservato** (32768...)</span><span class="sxs-lookup"><span data-stu-id="0ad84-199">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="0ad84-200"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ad84-200"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0ad84-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ad84-201">Requirements</span></span>



| <span data-ttu-id="0ad84-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad84-202">Requirement</span></span> | <span data-ttu-id="0ad84-203">Valore</span><span class="sxs-lookup"><span data-stu-id="0ad84-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad84-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ad84-204">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad84-205">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0ad84-205">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0ad84-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ad84-206">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad84-207">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ad84-207">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0ad84-208">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ad84-208">Namespace</span></span><br/>                | <span data-ttu-id="0ad84-209">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0ad84-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0ad84-210">MOF</span><span class="sxs-lookup"><span data-stu-id="0ad84-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ad84-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ad84-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ad84-212">DLL</span><span class="sxs-lookup"><span data-stu-id="0ad84-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ad84-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ad84-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ad84-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ad84-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad84-215">**\_LANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="0ad84-215">**CIM\_LANEndpoint**</span></span>](cim-lanendpoint.md)
</dt> </dl>

 

