---
description: Contiene informazioni dettagliate su un'interfaccia richiesta da un client RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Struttura INTF_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527649"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="6e268-103">\_Struttura di voci INTF</span><span class="sxs-lookup"><span data-stu-id="6e268-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="6e268-104">\[**INTF \_ La voce** non è più supportata a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6e268-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6e268-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="6e268-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="6e268-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="6e268-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="6e268-107">Contiene informazioni dettagliate su un'interfaccia richiesta da un client RPC.</span><span class="sxs-lookup"><span data-stu-id="6e268-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e268-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e268-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="6e268-109">Members</span><span class="sxs-lookup"><span data-stu-id="6e268-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e268-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="6e268-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-111">Puntatore al GUID dell'interfaccia rappresentato come stringa Unicode nel formato seguente: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="6e268-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="6e268-112">**wszDescr**</span><span class="sxs-lookup"><span data-stu-id="6e268-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-113">Puntatore a una stringa che contiene la descrizione dell'interfaccia recuperata dal servizio di configurazione zero senza fili (WZCSVC).</span><span class="sxs-lookup"><span data-stu-id="6e268-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="6e268-114">**dwContext**</span><span class="sxs-lookup"><span data-stu-id="6e268-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-115">Riservato per utilizzo interno.</span><span class="sxs-lookup"><span data-stu-id="6e268-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-116">**ulMediaState**</span><span class="sxs-lookup"><span data-stu-id="6e268-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-117">Stato corrente di Connect di NDIS media per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="6e268-118">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="6e268-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="6e268-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="6e268-120">Significato</span><span class="sxs-lookup"><span data-stu-id="6e268-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="6e268-121"><dt> **Stato del supporto \_ \_ connesso**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="6e268-122">Il supporto è connesso.</span><span class="sxs-lookup"><span data-stu-id="6e268-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="6e268-123"><dt>**Supporto \_ di STATO \_ disconnesso**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="6e268-124">Il supporto è disconnesso.</span><span class="sxs-lookup"><span data-stu-id="6e268-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="6e268-125"><dt>**Supporto \_ di STATO \_ sconosciuto**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="6e268-126">Lo stato del supporto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6e268-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e268-127">**ulMediaType**</span><span class="sxs-lookup"><span data-stu-id="6e268-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-128">Tipi di supporto NDIS attualmente utilizzati dalla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6e268-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="6e268-129">Quando viene eseguita una query, il valore di questo membro è **NdisMedium802 \_ 3** come definito nel file di intestazione *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="6e268-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-130">**ulPhysicalMediaType**</span><span class="sxs-lookup"><span data-stu-id="6e268-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-131">Tipo di supporto NDIS per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="6e268-132">Quando viene eseguita una query, il valore di questo membro è **NdisPhysicalMediumWirelessLan** come definito nel file di intestazione *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="6e268-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-133">**nInfraMode**</span><span class="sxs-lookup"><span data-stu-id="6e268-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-134">La modalità di infrastruttura 802,11 corrente impostata sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-135">**nAuthMode**</span><span class="sxs-lookup"><span data-stu-id="6e268-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-136">La modalità di autenticazione 802,11 corrente impostata sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="6e268-137">La tabella seguente mostra i valori possibili per il parametro in base all'enumerazione della **\_ modalità di autenticazione NDIS 802 \_ 11 \_ \_** definita nel file di intestazione *NtDDNdis. h* .</span><span class="sxs-lookup"><span data-stu-id="6e268-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="6e268-138">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="6e268-139">Significato</span><span class="sxs-lookup"><span data-stu-id="6e268-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="6e268-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="6e268-141">Autenticazione di sistema aperta IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="6e268-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="6e268-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="6e268-143">Autenticazione condivisa IEEE 802,11 che usa una chiave di privacy equivalente cablata (WEP) pre-condivisa.</span><span class="sxs-lookup"><span data-stu-id="6e268-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="6e268-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6e268-145">Modalità switch automatico.</span><span class="sxs-lookup"><span data-stu-id="6e268-145">Auto-switch mode.</span></span> <span data-ttu-id="6e268-146">Quando si usa la modalità di commutazione automatica, la scheda di interfaccia di rete (NIC) wireless tenta prima di tutto la modalità di autenticazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="6e268-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="6e268-147">Se la modalità condivisa non riesce, la scheda di interfaccia di rete tenterà di utilizzare la modalità di autenticazione aperta.</span><span class="sxs-lookup"><span data-stu-id="6e268-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="6e268-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="6e268-149">Sicurezza WPA (Wireless Protected Access).</span><span class="sxs-lookup"><span data-stu-id="6e268-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="6e268-150">Viene eseguita l'autenticazione tra il richiedente, l'autenticatore e il server di autenticazione tramite IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="6e268-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="6e268-151">Le chiavi di crittografia sono dinamiche e derivano dal processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6e268-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="6e268-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="6e268-153">Sicurezza WPA con una chiave precondivisa.</span><span class="sxs-lookup"><span data-stu-id="6e268-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="6e268-154">Viene eseguita l'autenticazione tra il richiedente e l'autenticatore tramite IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="6e268-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="6e268-155">Le chiavi di crittografia sono dinamiche e derivano tramite la chiave precondivisa usata dal supplicant e dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="6e268-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="6e268-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="6e268-157">Sicurezza WPA.</span><span class="sxs-lookup"><span data-stu-id="6e268-157">WPA security.</span></span> <span data-ttu-id="6e268-158">L'autenticazione viene eseguita utilizzando una chiave precondivisa senza l'autenticazione IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="6e268-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="6e268-159">Le chiavi di crittografia sono statiche e derivano tramite la chiave precondivisa.</span><span class="sxs-lookup"><span data-stu-id="6e268-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="6e268-160">Questa modalità è applicabile solo ai tipi di rete ad hoc.</span><span class="sxs-lookup"><span data-stu-id="6e268-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="6e268-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="6e268-162">Sicurezza WPA2.</span><span class="sxs-lookup"><span data-stu-id="6e268-162">WPA2 security.</span></span> <span data-ttu-id="6e268-163">Viene eseguita l'autenticazione tra il richiedente, l'autenticatore e il server di autenticazione tramite IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="6e268-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="6e268-164">Le chiavi di crittografia sono dinamiche e derivano dal processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6e268-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="6e268-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="6e268-166">Specifica la sicurezza WPA2.</span><span class="sxs-lookup"><span data-stu-id="6e268-166">Specifies WPA2 security.</span></span> <span data-ttu-id="6e268-167">Viene eseguita l'autenticazione tra il richiedente e l'autenticatore tramite IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="6e268-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="6e268-168">Le chiavi di crittografia sono dinamiche e derivano tramite la chiave precondivisa usata dal supplicant e dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="6e268-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="6e268-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="6e268-170">Valore massimo possibile per il valore di enumerazione della **\_ modalità di autenticazione NDIS 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="6e268-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="6e268-171">Non si tratta di un valore valido per la modalità di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6e268-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="6e268-172">**nWepStatus**</span><span class="sxs-lookup"><span data-stu-id="6e268-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-173">La modalità di crittografia 802,11 corrente impostata sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-174">**dwCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="6e268-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-175">Valore di maschera di flag di controllo che indica il funzionamento di WZCSVC sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="6e268-176">La tabella seguente illustra i possibili valori di bit.</span><span class="sxs-lookup"><span data-stu-id="6e268-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="6e268-177">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="6e268-178">Significato</span><span class="sxs-lookup"><span data-stu-id="6e268-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="6e268-179"><dt>**INTFCTL \_ 0x0007 \_ mask cm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6e268-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="6e268-180">Maschera di maschera per la modalità filtro di rete.</span><span class="sxs-lookup"><span data-stu-id="6e268-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="6e268-181">INTFCTL \_ cm \_ mask & dwCtlFlags genera un valore del tipo di infrastruttura di \_ rete NDIS 802 \_ 11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6e268-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="6e268-182">Il valore risultante indica se WZCSVC si connette solo alle reti dell'infrastruttura, alle reti ad hoc o a entrambi i tipi di reti.</span><span class="sxs-lookup"><span data-stu-id="6e268-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="6e268-183"><dt>**INTFCTL \_**</dt> <dt>0x8000</dt> abilitato</span><span class="sxs-lookup"><span data-stu-id="6e268-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="6e268-184">Indica se WZCSVC deve configurare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="6e268-185"><dt>**INTFCTL \_**</dt> <dt>0X4000</dt> di fallback</span><span class="sxs-lookup"><span data-stu-id="6e268-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="6e268-186">Se non è disponibile una rete preferita, questo valore indica se WZCSVC deve configurare automaticamente la scheda di interfaccia di rete da associare a qualsiasi rete disponibile.</span><span class="sxs-lookup"><span data-stu-id="6e268-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="6e268-187"><dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="6e268-188">Indica se il driver NIC supporta tutti i OID 802,11 necessari per il funzionamento di WZCSVC.</span><span class="sxs-lookup"><span data-stu-id="6e268-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="6e268-189"><dt>0x1000</dt> <dt> **\_ volatile INTFCTL**</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="6e268-190">Indica se i parametri del servizio per questa interfaccia devono essere conservati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6e268-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="6e268-191">Se questo valore è impostato, questi parametri sono volatili e non devono essere conservati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6e268-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="6e268-192"><dt> **\_ Criteri INTFCTL**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="6e268-193">Indica se i parametri del servizio per questa interfaccia vengono inseriti da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6e268-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="6e268-194">Se questo valore è impostato, i parametri del servizio vengono inseriti nel computer locale tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6e268-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="6e268-195"><dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="6e268-196">Indica se il supporto 802.1 X è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6e268-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="6e268-197">**dwDynFlags**</span><span class="sxs-lookup"><span data-stu-id="6e268-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-198">Maschera di bit dei flag dinamici che controllano il comportamento dinamico (non persistente e non statico) nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="6e268-199">Questi bit sono utili per attivare modifiche temporanee e dinamiche nel modo in cui WZCSVC agisce sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="6e268-200">Nessuno di questi bit è salvato in modo permanente nel registro di sistema, quindi le impostazioni non sopravvivono a un riavvio del sistema o una sequenza di disabilitazione e abilitazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6e268-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="6e268-201">La tabella seguente illustra i possibili valori di bit.</span><span class="sxs-lookup"><span data-stu-id="6e268-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="6e268-202">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="6e268-203">Significato</span><span class="sxs-lookup"><span data-stu-id="6e268-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="6e268-204"><dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6e268-205">Indica che WZCSVC non deve richiedere all'interfaccia di eseguire un'analisi attiva, ma usare invece i valori memorizzati nella cache nel driver NIC.</span><span class="sxs-lookup"><span data-stu-id="6e268-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e268-206">**dwCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6e268-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-207">Specifica le funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="6e268-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="6e268-208">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="6e268-209">Significato</span><span class="sxs-lookup"><span data-stu-id="6e268-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="6e268-210"><dt>**INTFCAP \_ \_ \_ Maschera di crittografia max**</dt> <dt>0x000000FF</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="6e268-211">I bit di ordine inferiore di questo membro vengono usati per indicare la crittografia massima supportata.</span><span class="sxs-lookup"><span data-stu-id="6e268-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="6e268-212">I valori possibili sono alcuni dei valori di enumerazione definiti nella struttura **di \_ \_ \_ \_ stato WEP NDIS 802 11** nel file di intestazione *NtDDNdis. h* incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6e268-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="6e268-213">Il \_ valore 11Encryption1Enabled di Ndis802 (2) indica che il protocollo WEP è supportato.</span><span class="sxs-lookup"><span data-stu-id="6e268-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="6e268-214">TKIP e AES non sono supportati e una chiave di trasmissione potrebbe essere disponibile o meno.</span><span class="sxs-lookup"><span data-stu-id="6e268-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="6e268-215">Il \_ valore 11Encryption2Enabled di Ndis802 (9) indica che TKIP e WEP sono supportati.</span><span class="sxs-lookup"><span data-stu-id="6e268-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="6e268-216">AES non è supportato ed è disponibile una chiave di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="6e268-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="6e268-217">Il \_ valore Ndis802 11Encryption3Enabled (11) indica che AES, TKIP e WEP sono supportati e che è disponibile una chiave di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="6e268-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="6e268-218">Ndis802 \_ 11EncryptionNotSupported (8) indica che la chiave WEP non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6e268-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="6e268-219"><dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN</span><span class="sxs-lookup"><span data-stu-id="6e268-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="6e268-220">Indica il supporto per la rete sicura semplice (SSN), che è un subset di 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="6e268-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="6e268-221">Il SSN modifica periodicamente la chiave di crittografia, anziché lo standard WEP (Wired equivalente privacy), che usa una chiave statica.</span><span class="sxs-lookup"><span data-stu-id="6e268-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="6e268-222">Affinché il SSN funzioni, la crittografia massima supportata deve essere almeno TKIP.</span><span class="sxs-lookup"><span data-stu-id="6e268-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="6e268-223">Il SSN è stato sviluppato da un consorzio di fornitori nel 2002 come approccio provvisorio per migliorare la sicurezza della LAN wireless durante il completamento dello standard IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="6e268-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="6e268-224"><dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="6e268-225">Indica il supporto per lo standard IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="6e268-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="6e268-226">**rdNicCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6e268-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-227">Un set di funzionalità per 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="6e268-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="6e268-228">La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdNicCapabilities** quando viene chiamato con il flag delle **\_ funzionalità INTF** passato nel parametro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="6e268-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="6e268-229">Se la chiamata di funzione ha esito positivo, il membro **pData** della struttura di **\_ dati non elaborati** contiene una struttura di **\_ \_ funzionalità INTF 80211** .</span><span class="sxs-lookup"><span data-stu-id="6e268-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-230">**rdSSID**</span><span class="sxs-lookup"><span data-stu-id="6e268-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-231">Dati binari contenenti l'SSID 802,11 attualmente configurato nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="6e268-232">La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdSSID** quando viene chiamato con il flag **\_ SSID INTF** passato nel parametro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="6e268-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="6e268-233">Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene il membro **SsidLength** di una struttura **\_ SSID NDIS 802 \_ \_ 11** e il membro **pData** della struttura di **\_ dati non elaborati** contiene il membro **SSID** di una struttura **\_ \_ \_ SSID 802 11 di NDIS** .</span><span class="sxs-lookup"><span data-stu-id="6e268-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="6e268-234">La struttura dell' **\_ \_ \_ SSID NDIS 802 11** viene definita nel file di intestazione *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="6e268-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-235">**rdBSSID**</span><span class="sxs-lookup"><span data-stu-id="6e268-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-236">Dati binari contenenti l'BSSID 802,11 configurato nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="6e268-237">La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdBSSID** quando viene chiamato con il flag **\_ BSSID di INTF** passato nel parametro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="6e268-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="6e268-238">Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la dimensione di una struttura di **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** e il membro **pData** della struttura di **\_ dati non elaborati** contiene la struttura degli **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** .</span><span class="sxs-lookup"><span data-stu-id="6e268-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="6e268-239">La struttura degli **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** viene definita nel file di intestazione *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="6e268-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-240">**rdBSSIDList**</span><span class="sxs-lookup"><span data-stu-id="6e268-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-241">Dati binari che contengono l'elenco di BSSIDs recuperato per ultimo da WZCSVC.</span><span class="sxs-lookup"><span data-stu-id="6e268-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="6e268-242">La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdBSSIDList** quando viene chiamato con il flag **\_ BSSIDLIST di INTF** passato nel parametro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="6e268-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="6e268-243">Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la lunghezza del buffer con i dati restituiti e il membro **PData** della struttura di **\_ dati non elaborati** contiene la struttura dell' **elenco di \_ configurazione WZC 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="6e268-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-244">**rdStSSIDList**</span><span class="sxs-lookup"><span data-stu-id="6e268-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-245">Dati binari che contengono l'elenco di reti preferite configurate per questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="6e268-246">La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdStSSIDList** quando viene chiamato con il flag **\_ PREFLIST di INTF** passato nel parametro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="6e268-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="6e268-247">Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la lunghezza del buffer con i dati restituiti e il membro **PData** della struttura di **\_ dati non elaborati** contiene la struttura dell' **elenco di \_ configurazione WZC 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="6e268-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="6e268-248">Se una delle reti preferite è attualmente connessa, per il membro **dwCtlFlags** della struttura **di \_ \_ Configurazione WLAN WZC** per la rete verrà impostato il bit **WZCCTL \_ media \_ Connected** (0x0400).</span><span class="sxs-lookup"><span data-stu-id="6e268-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="6e268-249">**rdCtrlData**</span><span class="sxs-lookup"><span data-stu-id="6e268-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="6e268-250">Dati binari usati con altri flag di controllo quando si impostano parametri aggiuntivi sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e268-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e268-251">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e268-251">Remarks</span></span>

<span data-ttu-id="6e268-252">La struttura di **\_ immissione INTF** viene utilizzata dalle funzioni [**WZCQueryInterface**](wzcqueryinterface.md) e [**WZCRefreshInterface**](wzcrefreshinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="6e268-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="6e268-253">La **struttura \_ dei dati non elaborati** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6e268-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="6e268-254">Il membro *pData* punta ai dati binari.</span><span class="sxs-lookup"><span data-stu-id="6e268-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="6e268-255">*DwDataLen* indica il numero di byte a cui punta *pData*.</span><span class="sxs-lookup"><span data-stu-id="6e268-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="6e268-256">Il file di intestazione *wzcsapi. h* non è disponibile nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6e268-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e268-257">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e268-257">Requirements</span></span>



| <span data-ttu-id="6e268-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e268-258">Requirement</span></span> | <span data-ttu-id="6e268-259">Valore</span><span class="sxs-lookup"><span data-stu-id="6e268-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e268-260">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e268-260">Minimum supported client</span></span><br/> | <span data-ttu-id="6e268-261">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e268-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e268-262">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e268-262">Minimum supported server</span></span><br/> | <span data-ttu-id="6e268-263">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e268-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e268-264">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6e268-264">End of client support</span></span><br/>    | <span data-ttu-id="6e268-265">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="6e268-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="6e268-266">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6e268-266">End of server support</span></span><br/>    | <span data-ttu-id="6e268-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e268-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="6e268-268">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e268-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e268-269"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e268-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e268-270">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e268-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e268-271">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="6e268-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="6e268-272">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="6e268-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="6e268-273">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="6e268-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




