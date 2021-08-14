---
description: Fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio Wireless Zero Configuration.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Funzione WZCQueryInterface (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3dd7ce876501486b9bec4dbad63ce5812b910b32b9dcdaa1eb80aff3e7cc415e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797411"
---
# <a name="wzcqueryinterface-function"></a>Funzione WZCQueryInterface

\[**WZCQueryInterface** non è più supportato a Windows Vista e Windows Server 2008. Usare invece [**la funzione WlanQueryInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) Per altre informazioni, vedere [Informazioni sull'API Wi-Fi nativa.](about-the-native-wifi-api.md) \]

La **funzione WZCQueryInterface** fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio Wireless Zero Configuration.

Fornisce informazioni dettagliate per una determinata interfaccia.

## <a name="syntax"></a>Sintassi


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrvAddr* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa contenente il nome del computer in cui eseguire questa funzione. Se questo parametro è **NULL,** nel computer locale viene eseguita una query sul servizio Wireless Zero Configuration.

Se il *parametro pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*dwInFlags* \[ Pollici\]
</dt> <dd>

Campi su cui eseguire query. Si tratta di una maschera di bit che può contenere qualsiasi combinazione dei flag seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | Restituisce il valore per **il membro dwDynFlags** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ Descr**</dt> <dt>0x00010000</dt> </dl>                      | Restituisce il valore per il **membro wszDescr** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | Restituisce i valori per i membri **ulMediaState**, **ulMediaType** e **ulPhysicalMediaType** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PREFLIST**</dt> <dt>0x00040000</dt> </dl>             | Restituisce l'elenco preferito di reti nel membro **rdStSSIDList** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ FUNZIONALITÀ**</dt> <dt>0x00080000</dt> </dl> | Restituisce i valori per **i membri dwCapabilities** e **rdNicCapabilities** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ INFRAMODE**</dt> <dt>0x00200000</dt> </dl>          | Restituisce il valore per il **membro nInfraMode** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/> Il **membro nInfraMode** è valido solo in alcuni stati del contesto dell'interfaccia.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | Restituisce il valore per il **membro nAuthMode** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.* <br/> Il **membro nAuthMode** è valido solo in alcuni stati del contesto dell'interfaccia.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | Restituisce il valore per il **membro nWepStatus** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.* <br/> Il **membro nWepStatus** è valido solo in alcuni stati del contesto dell'interfaccia.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Restituisce il valore per **il membro rdSSID** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/> Il **membro rdSSID** è valido solo in alcuni stati del contesto dell'interfaccia.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Restituisce il valore per **il membro rdBSSID** nella struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/> Il **membro rdBSSID** è valido solo in alcuni stati del contesto dell'interfaccia.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | Restituisce l'elenco visibile delle reti nel membro **rdBSSIDList** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf.*<br/> Il **membro rdBSSIDList** è valido solo in alcuni stati del contesto dell'interfaccia.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

In input, puntatore alla chiave dell'interfaccia su cui eseguire una query. Nell'output, puntatore ai dati dell'interfaccia richiesti. Questo parametro è un puntatore a una [**struttura INTF \_ ENTRY.**](intf-entry.md)

</dd> <dt>

*pdwOutFlags* \[ Cambio\]
</dt> <dd>

Un set di campi è stato recuperato correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici restituiti seguenti.



| Codice restituito                                                                                               | Descrizione                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ \_ NELL'AMBITO DEL CESTINO**</dt> </dl>      | I blocchi di controllo di archiviazione sono stati distrutti. Questo errore viene restituito se il servizio Wireless Zero Configuration non ha inizializzato oggetti interni.<br/>                                                                                                                      |
| <dl> <dt>**FILE \_ DI ERRORE NON \_ \_ TROVATO**</dt> </dl>    | Non è possibile trovare il file specificato. Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* non corrisponde a nessuna delle interfacce LAN wireless nel computer locale. <br/> |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>  | Un parametro non è corretto. Questo errore viene restituito se il *parametro pIntf* è **NULL.** Questo errore viene restituito se il **membro wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* è **NULL.** <br/>                            |
| <dl> <dt>**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**</dt> </dl> | Memoria insufficiente per elaborare la richiesta e allocare memoria per i risultati della query.<br/>                                                                                                                                                                       |
| <dl> <dt>**STATO \_ RPC**</dt> </dl>                | Vari codici di errore.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il **membro wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless. È possibile recuperare un elenco di interfacce LAN wireless chiamando la [**funzione WZCEnumInterfaces.**](wzcenuminterfaces.md)

I membri seguenti della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta *pIntf* devono essere impostati su 0 prima di una chiamata alla funzione **WZCQueryInterface:** **rdSSID,** **rdBSSID,** **rdBSSIDList,** **rdStSSIDList** **e rdCtrlData.**

Il servizio Wireless Zero Configuration non aggiorna automaticamente lo stato dei supporti, anche quando vengono ricevuti eventi di supporto connessi e disconnessi. Un'applicazione deve forzare un aggiornamento dello stato multimediale chiamando la funzione [**WZCRefreshInterface**](wzcrefreshinterface.md) prima di chiamare la funzione **WZCQueryInterface** se lo stato del supporto NDIS deve essere richiesto (il bit INTF NDISMEDIA verrà impostato nel \_ parametro *dwInFlags).*

Quando il *parametro dwInFlags* contiene **INTF \_ BSSIDLIST,** la funzione **WZCQueryInterface** non imposta *dwOutFlags* con **INTF \_ BSSIDLIST** se l'elenco visibile delle reti è vuoto. Quando il *parametro dwInFlags* contiene **INTF \_ SSID,** la funzione **WZCQueryInterface** non imposta *dwOutFlags* con **\_ SSID INTF** se non è disponibile alcun SSID.

Se la funzione **WZCQueryInterface** restituisce ERROR SUCCESS, il chiamante deve chiamare la funzione \_ [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) con il *parametro pIntf* per rilasciare i buffer interni allocati per i dati restituiti quando queste informazioni non sono più necessarie. In questo modo vengono rilasciati i buffer usati dai membri **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** e **rdCtrlData** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta *il parametro pIntf.*

> [!Note]  
> Il file *di intestazione Wzcsapi.h* e il file della libreria di importazione *Wzcsapi.lib* non sono disponibili in Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                         |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VOCE \_ INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
