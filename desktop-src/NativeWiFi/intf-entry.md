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
# <a name="intf_entry-structure"></a>\_Struttura di voci INTF

\[**INTF \_ La voce** non è più supportata a partire da Windows Vista e Windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

Contiene informazioni dettagliate su un'interfaccia richiesta da un client RPC.

## <a name="syntax"></a>Sintassi


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



## <a name="members"></a>Members

<dl> <dt>

**wszGuid**
</dt> <dd>

Puntatore al GUID dell'interfaccia rappresentato come stringa Unicode nel formato seguente: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> <dt>

**wszDescr**
</dt> <dd>

Puntatore a una stringa che contiene la descrizione dell'interfaccia recuperata dal servizio di configurazione zero senza fili (WZCSVC).

</dd> <dt>

**dwContext**
</dt> <dd>

Riservato per utilizzo interno.

</dd> <dt>

**ulMediaState**
</dt> <dd>

Stato corrente di Connect di NDIS media per l'interfaccia. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                  | Significato                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **Stato del supporto \_ \_ connesso**</dt> <dt>1</dt> </dl>       | Il supporto è connesso.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**Supporto \_ di STATO \_ disconnesso**</dt> <dt>0</dt> </dl> | Il supporto è disconnesso.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**Supporto \_ di STATO \_ sconosciuto**</dt> <dt>-1</dt> </dl>               | Lo stato del supporto è sconosciuto.<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

Tipi di supporto NDIS attualmente utilizzati dalla scheda di interfaccia di rete. Quando viene eseguita una query, il valore di questo membro è **NdisMedium802 \_ 3** come definito nel file di intestazione *Ndispnp. h* .

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

Tipo di supporto NDIS per l'interfaccia. Quando viene eseguita una query, il valore di questo membro è **NdisPhysicalMediumWirelessLan** come definito nel file di intestazione *Ndispnp. h* .

</dd> <dt>

**nInfraMode**
</dt> <dd>

La modalità di infrastruttura 802,11 corrente impostata sull'interfaccia.

</dd> <dt>

**nAuthMode**
</dt> <dd>

La modalità di autenticazione 802,11 corrente impostata sull'interfaccia.

La tabella seguente mostra i valori possibili per il parametro in base all'enumerazione della **\_ modalità di autenticazione NDIS 802 \_ 11 \_ \_** definita nel file di intestazione *NtDDNdis. h* .



| Valore                                                                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt> </dl>                         | Autenticazione di sistema aperta IEEE 802,11.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | Autenticazione condivisa IEEE 802,11 che usa una chiave di privacy equivalente cablata (WEP) pre-condivisa. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | Modalità switch automatico. Quando si usa la modalità di commutazione automatica, la scheda di interfaccia di rete (NIC) wireless tenta prima di tutto la modalità di autenticazione condivisa. Se la modalità condivisa non riesce, la scheda di interfaccia di rete tenterà di utilizzare la modalità di autenticazione aperta. <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             | Sicurezza WPA (Wireless Protected Access). Viene eseguita l'autenticazione tra il richiedente, l'autenticatore e il server di autenticazione tramite IEEE 802.1 X. Le chiavi di crittografia sono dinamiche e derivano dal processo di autenticazione. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | Sicurezza WPA con una chiave precondivisa. Viene eseguita l'autenticazione tra il richiedente e l'autenticatore tramite IEEE 802.1 X. Le chiavi di crittografia sono dinamiche e derivano tramite la chiave precondivisa usata dal supplicant e dall'autenticatore. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | Sicurezza WPA. L'autenticazione viene eseguita utilizzando una chiave precondivisa senza l'autenticazione IEEE 802.1 X. Le chiavi di crittografia sono statiche e derivano tramite la chiave precondivisa. Questa modalità è applicabile solo ai tipi di rete ad hoc. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | Sicurezza WPA2. Viene eseguita l'autenticazione tra il richiedente, l'autenticatore e il server di autenticazione tramite IEEE 802.1 X. Le chiavi di crittografia sono dinamiche e derivano dal processo di autenticazione. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | Specifica la sicurezza WPA2. Viene eseguita l'autenticazione tra il richiedente e l'autenticatore tramite IEEE 802 1X. Le chiavi di crittografia sono dinamiche e derivano tramite la chiave precondivisa usata dal supplicant e dall'autenticatore. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | Valore massimo possibile per il valore di enumerazione della **\_ modalità di autenticazione NDIS 802 \_ 11 \_ \_** . Non si tratta di un valore valido per la modalità di autenticazione. <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

La modalità di crittografia 802,11 corrente impostata sull'interfaccia.

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

Valore di maschera di flag di controllo che indica il funzionamento di WZCSVC sull'interfaccia.

La tabella seguente illustra i possibili valori di bit.



| Valore                                                                                                                                                                                                                                 | Significato                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_ 0x0007 \_ mask cm**</dt> <dt></dt> </dl>      | Maschera di maschera per la modalità filtro di rete. INTFCTL \_ cm \_ mask & dwCtlFlags genera un valore del tipo di infrastruttura di \_ rete NDIS 802 \_ 11 \_ \_ . Il valore risultante indica se WZCSVC si connette solo alle reti dell'infrastruttura, alle reti ad hoc o a entrambi i tipi di reti.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0x8000</dt> abilitato </dl>       | Indica se WZCSVC deve configurare l'interfaccia.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0X4000</dt> di fallback </dl>    | Se non è disponibile una rete preferita, questo valore indica se WZCSVC deve configurare automaticamente la scheda di interfaccia di rete da associare a qualsiasi rete disponibile.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | Indica se il driver NIC supporta tutti i OID 802,11 necessari per il funzionamento di WZCSVC.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt>0x1000</dt> <dt> **\_ volatile INTFCTL**</dt> </dl> | Indica se i parametri del servizio per questa interfaccia devono essere conservati nel registro di sistema. <br/> Se questo valore è impostato, questi parametri sono volatili e non devono essere conservati nel registro di sistema.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **\_ Criteri INTFCTL**</dt> <dt>0x0800</dt> </dl>       | Indica se i parametri del servizio per questa interfaccia vengono inseriti da criteri di gruppo.<br/> Se questo valore è impostato, i parametri del servizio vengono inseriti nel computer locale tramite criteri di gruppo.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | Indica se il supporto 802.1 X è abilitato.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

Maschera di bit dei flag dinamici che controllano il comportamento dinamico (non persistente e non statico) nell'interfaccia.

Questi bit sono utili per attivare modifiche temporanee e dinamiche nel modo in cui WZCSVC agisce sull'interfaccia. Nessuno di questi bit è salvato in modo permanente nel registro di sistema, quindi le impostazioni non sopravvivono a un riavvio del sistema o una sequenza di disabilitazione e abilitazione del dispositivo.

La tabella seguente illustra i possibili valori di bit.



| Valore                                                                                                                                                                                                                            | Significato                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt> </dl> | Indica che WZCSVC non deve richiedere all'interfaccia di eseguire un'analisi attiva, ma usare invece i valori memorizzati nella cache nel driver NIC.<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

Specifica le funzionalità del driver.



| Valore                                                                                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_ \_ \_ Maschera di crittografia max**</dt> <dt>0x000000FF</dt> </dl> | I bit di ordine inferiore di questo membro vengono usati per indicare la crittografia massima supportata. I valori possibili sono alcuni dei valori di enumerazione definiti nella struttura **di \_ \_ \_ \_ stato WEP NDIS 802 11** nel file di intestazione *NtDDNdis. h* incluso nel Windows SDK.<br/> Il \_ valore 11Encryption1Enabled di Ndis802 (2) indica che il protocollo WEP è supportato. TKIP e AES non sono supportati e una chiave di trasmissione potrebbe essere disponibile o meno. <br/> Il \_ valore 11Encryption2Enabled di Ndis802 (9) indica che TKIP e WEP sono supportati. AES non è supportato ed è disponibile una chiave di trasmissione. <br/> Il \_ valore Ndis802 11Encryption3Enabled (11) indica che AES, TKIP e WEP sono supportati e che è disponibile una chiave di trasmissione. <br/> Ndis802 \_ 11EncryptionNotSupported (8) indica che la chiave WEP non è supportata. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN </dl>                                       | Indica il supporto per la rete sicura semplice (SSN), che è un subset di 802.11 i. <br/> Il SSN modifica periodicamente la chiave di crittografia, anziché lo standard WEP (Wired equivalente privacy), che usa una chiave statica. Affinché il SSN funzioni, la crittografia massima supportata deve essere almeno TKIP. Il SSN è stato sviluppato da un consorzio di fornitori nel 2002 come approccio provvisorio per migliorare la sicurezza della LAN wireless durante il completamento dello standard IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | Indica il supporto per lo standard IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

Un set di funzionalità per 802.11 i.

La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdNicCapabilities** quando viene chiamato con il flag delle **\_ funzionalità INTF** passato nel parametro *dwInflags* . Se la chiamata di funzione ha esito positivo, il membro **pData** della struttura di **\_ dati non elaborati** contiene una struttura di **\_ \_ funzionalità INTF 80211** .

</dd> <dt>

**rdSSID**
</dt> <dd>

Dati binari contenenti l'SSID 802,11 attualmente configurato nell'interfaccia.

La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdSSID** quando viene chiamato con il flag **\_ SSID INTF** passato nel parametro *dwInflags* . Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene il membro **SsidLength** di una struttura **\_ SSID NDIS 802 \_ \_ 11** e il membro **pData** della struttura di **\_ dati non elaborati** contiene il membro **SSID** di una struttura **\_ \_ \_ SSID 802 11 di NDIS** .

La struttura dell' **\_ \_ \_ SSID NDIS 802 11** viene definita nel file di intestazione *Ntddndis. h* .

</dd> <dt>

**rdBSSID**
</dt> <dd>

Dati binari contenenti l'BSSID 802,11 configurato nell'interfaccia.

La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdBSSID** quando viene chiamato con il flag **\_ BSSID di INTF** passato nel parametro *dwInflags* . Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la dimensione di una struttura di **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** e il membro **pData** della struttura di **\_ dati non elaborati** contiene la struttura degli **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** .

La struttura degli **\_ \_ \_ \_ indirizzi MAC NDIS 802 11** viene definita nel file di intestazione *Ntddndis. h* .

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

Dati binari che contengono l'elenco di BSSIDs recuperato per ultimo da WZCSVC.

La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdBSSIDList** quando viene chiamato con il flag **\_ BSSIDLIST di INTF** passato nel parametro *dwInflags* . Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la lunghezza del buffer con i dati restituiti e il membro **PData** della struttura di **\_ dati non elaborati** contiene la struttura dell' **elenco di \_ configurazione WZC 802 \_ 11 \_ \_** .

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

Dati binari che contengono l'elenco di reti preferite configurate per questa interfaccia.

La funzione [**WZCQueryInterface**](wzcqueryinterface.md) restituisce dati **rdStSSIDList** quando viene chiamato con il flag **\_ PREFLIST di INTF** passato nel parametro *dwInflags* . Se la chiamata di funzione ha esito positivo, il membro **dwDataLen** della struttura di **\_ dati non elaborati** contiene la lunghezza del buffer con i dati restituiti e il membro **PData** della struttura di **\_ dati non elaborati** contiene la struttura dell' **elenco di \_ configurazione WZC 802 \_ 11 \_ \_** .

Se una delle reti preferite è attualmente connessa, per il membro **dwCtlFlags** della struttura **di \_ \_ Configurazione WLAN WZC** per la rete verrà impostato il bit **WZCCTL \_ media \_ Connected** (0x0400).

</dd> <dt>

**rdCtrlData**
</dt> <dd>

Dati binari usati con altri flag di controllo quando si impostano parametri aggiuntivi sull'interfaccia.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura di **\_ immissione INTF** viene utilizzata dalle funzioni [**WZCQueryInterface**](wzcqueryinterface.md) e [**WZCRefreshInterface**](wzcrefreshinterface.md) .

La **struttura \_ dei dati non elaborati** viene definita nel modo seguente:


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



Il membro *pData* punta ai dati binari. *DwDataLen* indica il numero di byte a cui punta *pData*.

> [!Note]  
> Il file di intestazione *wzcsapi. h* non è disponibile nel Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                       |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




