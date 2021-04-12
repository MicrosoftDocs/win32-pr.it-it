---
description: Aggiorna le informazioni sull'interfaccia per una specifica interfaccia LAN wireless.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Funzione WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348111"
---
# <a name="wzcrefreshinterface-function"></a>WZCRefreshInterface (funzione)

\[**WZCRefreshInterface** non è supportato a partire da Windows Vista e windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

La funzione **WZCRefreshInterface** aggiorna le informazioni sull'interfaccia per una specifica interfaccia LAN wireless.

## <a name="syntax"></a>Sintassi


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrvAddr* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione. Se questo parametro è **null**, il servizio di configurazione zero senza fili viene chiamato sul computer locale.

Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*dwInFlags* \[ in\]
</dt> <dd>

Set di campi da aggiornare insieme a specifiche azioni di aggiornamento da eseguire. Si tratta di una maschera di maschera che può contenere qualsiasi combinazione dei flag seguenti.



| Valore                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ 0x00010000 DESCr**</dt> <dt></dt> </dl>             | Aggiornare la descrizione dell'interfaccia per un'interfaccia LAN wireless.<br/> La descrizione dell'interfaccia aggiornata può essere recuperata chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ Descr** impostato nel parametro *dwInFlags* . La descrizione dell'interfaccia viene restituita nel membro **wszDescr** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* restituito dalla funzione **WZCQueryInterface** .<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_**</dt> <dt>0x00020000</dt> NDISMEDIA </dl> | Aggiornare le informazioni sui supporti NDIS per un'interfaccia LAN wireless.<br/> Le informazioni sul supporto NDIS aggiornate possono essere recuperate chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ NDISMEDIA** impostato nel parametro *dwInFlags* . Le informazioni sui supporti NDIS vengono restituite nei membri **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* restituito dalla funzione **WZCQueryInterface** .<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ TUTTI \_ OID**</dt> <dt>0xFFF00000</dt> </dl>   | Aggiornare tutti i OID NDIS per un'interfaccia LAN wireless. Questa opzione consente di aggiornare la maggior parte dei dati per un'interfaccia LAN wireless.<br/> Le informazioni aggiornate possono essere recuperate chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) .<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ voci INTF**](intf-entry.md) che contiene la chiave dell'interfaccia da aggiornare.

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Set di campi che sono stati aggiornati correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti codici restituiti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE nell' \_ Arena \_**</dt> </dl>     | I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente. Questo errore viene restituito se il servizio di configurazione zero senza fili non ha inizializzato gli oggetti interni.<br/>                                                                                                                      |
| <dl> <dt>**FILE di errore \_ \_ non \_ trovato**</dt> </dl>   | Non è possibile trovare il file specificato. Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura di [**\_ immissione INTF**](intf-entry.md) a cui punta il parametro *PINTF* non corrisponde ad alcuna interfaccia LAN wireless nel computer locale. <br/> |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl> | Un parametro non è corretto. Questo errore viene restituito se il parametro *pIntf* è **null**. Questo errore viene restituito se il membro **wszGuid** della struttura [**di \_ voce INTF**](intf-entry.md) a cui punta il parametro *pIntf* è **null**. <br/>                            |
| <dl> <dt>**\_stato RPC**</dt> </dl>               | Codici di errore diversi.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il membro **wszGuid** della struttura [**di \_ immissione INTF**](intf-entry.md) a cui punta il parametro *pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless. È possibile recuperare un elenco di interfacce LAN wireless chiamando la funzione [**WZCEnumInterfaces**](wzcenuminterfaces.md) .

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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**\_voce INTF**](intf-entry.md)
</dt> </dl>

 

 




