---
description: Fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio di configurazione wireless zero.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Funzione WZCQueryInterface (wzcsapi. h)
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
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884546"
---
# <a name="wzcqueryinterface-function"></a>WZCQueryInterface (funzione)

\[**WZCQueryInterface** non è più supportato a partire da Windows Vista e windows Server 2008. Usare invece la funzione [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) . Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md). \]

La funzione **WZCQueryInterface** fornisce informazioni dettagliate per un'interfaccia LAN wireless gestita dal servizio di configurazione wireless zero.

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

*pSrvAddr* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione. Se questo parametro è **null**, viene eseguita una query sul servizio di configurazione zero wireless nel computer locale.

Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*dwInFlags* \[ in\]
</dt> <dd>

Campi su cui eseguire la query. Si tratta di una maschera di maschera che può contenere qualsiasi combinazione dei flag seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_**</dt> <dt>0x00000010</dt> DYNFLAGS </dl>             | Restituisce il valore per il membro **dwDynFlags** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ 0x00010000 DESCr**</dt> <dt></dt> </dl>                      | Restituisce il valore per il membro **wszDescr** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_**</dt> <dt>0x00020000</dt> NDISMEDIA </dl>          | Restituisce i valori per i membri **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** nella struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_**</dt> <dt>0x00040000</dt> PREFLIST </dl>             | Restituisce l'elenco preferito di reti nel membro **rdStSSIDList** della struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ FUNZIONALITÀ**</dt> <dt>0x00080000</dt> </dl> | Restituisce i valori per i membri **dwCapabilities** e **rdNicCapabilities** nella struttura di [**\_ voci INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_**</dt> <dt>0x00200000</dt> INFRAMODE </dl>          | Restituisce il valore per il membro **nInfraMode** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/> Il membro **nInfraMode** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_**</dt> <dt>0x00400000</dt> AUTHMODE </dl>             | Restituisce il valore per il membro **nAuthMode** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* . <br/> Il membro **nAuthMode** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_**</dt> <dt>0x00800000</dt> WEPSTATUS </dl>          | Restituisce il valore per il membro **nWepStatus** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* . <br/> Il membro **nWepStatus** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Restituisce il valore per il membro **rdSSID** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/> Il membro **rdSSID** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_**</dt> <dt>0x02000000</dt> BSSID </dl>                      | Restituisce il valore per il membro **rdBSSID** nella struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/> Il membro **rdBSSID** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_**</dt> <dt>0x04000000</dt> BSSIDLIST </dl>          | Restituisce l'elenco visibile di reti nel membro **rdBSSIDList** della struttura di [**\_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* .<br/> Il membro **rdBSSIDList** è valido solo in alcuni Stati del contesto dell'interfaccia.<br/> |



 

</dd> <dt>

*pIntf* \[ in uscita\]
</dt> <dd>

In input, puntatore alla chiave dell'interfaccia su cui eseguire una query. Nell'output, puntatore ai dati dell'interfaccia richiesta. Questo parametro è un puntatore a una struttura di [**\_ voce INTF**](intf-entry.md) .

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Set di campi recuperato correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.



| Codice restituito                                                                                               | Descrizione                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE nell' \_ Arena \_**</dt> </dl>      | I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente. Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.<br/>                                                                                                                      |
| <dl> <dt>**FILE di errore \_ \_ non \_ trovato**</dt> </dl>    | Non è possibile trovare il file specificato. Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *PINTF* non corrisponde ad alcuna interfaccia LAN wireless nel computer locale. <br/> |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>  | Un parametro non è corretto. Questo errore viene restituito se il parametro *pIntf* è **null**. Questo errore viene restituito se il membro **wszGuid** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* è **null**. <br/>                            |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl> | Memoria insufficiente per elaborare la richiesta e allocare memoria per i risultati della query.<br/>                                                                                                                                                                       |
| <dl> <dt>**\_stato RPC**</dt> </dl>                | Codici di errore diversi.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il membro **wszGuid** della struttura [**di \_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless. È possibile recuperare un elenco di interfacce LAN wireless chiamando la funzione [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

I membri seguenti della struttura [**di \_ voci INTF**](intf-entry.md) a cui punta *pIntf* devono essere impostati su 0 prima di una chiamata alla funzione **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** e **rdCtrlData**.

Il servizio di configurazione zero senza fili non automotically lo stato di aggiornamento dei supporti, anche quando vengono ricevuti gli eventi di supporto connessi e disconnessi. Un'applicazione deve forzare un aggiornamento dello stato multimediale chiamando la funzione [**WZCRefreshInterface**](wzcrefreshinterface.md) prima di chiamare la funzione **WZCQueryInterface** se è necessario richiedere lo stato del supporto NDIS (il \_ bit NDISMEDIA di INTF verrà impostato nel parametro *dwInFlags* ).

Quando il parametro *dwInFlags* contiene **INTF \_ BSSIDLIST**, la funzione **WZCQueryInterface** non imposta la *dwOutFlags* con **INTF \_ BSSIDLIST** se l'elenco di reti visibile è vuoto. Quando il parametro *dwInFlags* contiene **INTF \_ SSID**, la funzione **WZCQueryInterface** non imposta *dwOutFlags* con **INTF \_ SSID** se non è disponibile alcun SSID.

Se la funzione **WZCQueryInterface** restituisce l'errore \_ Success, il chiamante deve chiamare la funzione [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) con il parametro *pIntf* per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie. In questo modo vengono rilasciati i buffer usati dai membri **rdSSID**, **rdBSSID**, **rdBSSIDList**, **RdStSSIDList** e **rdCtrlData** della struttura di [**\_ voci INTF**](intf-entry.md) a cui punta il parametro *pIntf* .

> [!Note]  
> Il file di intestazione *wzcsapi. h* e il file della libreria di importazione *wzcsapi. lib* non sono disponibili nel Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                         |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_voce INTF**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
