---
description: Aggiorna le informazioni sull'interfaccia per un'interfaccia LAN wireless specifica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Funzione WZCRefreshInterface (Wzcsapi.h)
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
ms.openlocfilehash: 43f2b35215c930517d5352073c679a116388eb49aaa3bd6a3c567467e50be1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064511"
---
# <a name="wzcrefreshinterface-function"></a>Funzione WZCRefreshInterface

\[**WZCRefreshInterface** non è supportato a Windows Vista e Windows Server 2008. Usare invece [l'API Wi-Fi nativa](native-wifi-reference.md), che offre funzionalità simili. Per altre informazioni, vedere [Informazioni sull'API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **funzione WZCRefreshInterface aggiorna** le informazioni sull'interfaccia per un'interfaccia LAN wireless specifica.

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

*pSrvAddr* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa contenente il nome del computer in cui eseguire questa funzione. Se questo parametro è **NULL,** viene chiamato il servizio Wireless Zero Configuration nel computer locale.

Se il *parametro pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*dwInFlags* \[ Pollici\]
</dt> <dd>

Set di campi da aggiornare insieme ad azioni di aggiornamento specifiche da eseguire. Si tratta di una maschera di bit che può contenere qualsiasi combinazione dei flag seguenti.



| Valore                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ Descr**</dt> <dt>0x00010000</dt> </dl>             | Aggiornare la descrizione dell'interfaccia per un'interfaccia LAN wireless.<br/> La descrizione dell'interfaccia aggiornata può essere recuperata chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ DESCR** impostato nel *parametro dwInFlags.* La descrizione dell'interfaccia viene restituita nel membro **wszDescr** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* restituito dalla **funzione WZCQueryInterface.**<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Aggiornare le informazioni sui supporti NDIS per un'interfaccia LAN wireless.<br/> Le informazioni sui supporti NDIS aggiornate possono essere recuperate chiamando la funzione [**WZCQueryInterface**](wzcqueryinterface.md) con il bit **INTF \_ NDISMEDIA** impostato nel *parametro dwInFlags.* Le informazioni sui supporti NDIS vengono restituite nei membri **ulMediaState**, **ulMediaType** e **ulPhysicalMediaType** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* restituito dalla **funzione WZCQueryInterface.**<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ ALL \_ OIDS**</dt> <dt>0xFFF00000</dt> </dl>   | Aggiornare tutti gli OID NDIS per un'interfaccia LAN wireless. Questa opzione aggiorna la maggior parte dei dati per un'interfaccia LAN wireless.<br/> Le informazioni aggiornate possono essere recuperate chiamando la [**funzione WZCQueryInterface.**](wzcqueryinterface.md)<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura INTF \_ ENTRY**](intf-entry.md) contenente la chiave dell'interfaccia da aggiornare.

</dd> <dt>

*pdwOutFlags* \[ Cambio\]
</dt> <dd>

Set di campi aggiornati correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito può essere uno dei codici restituiti seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PIÙ \_ CESTINO**</dt> </dl>     | I blocchi di controllo di archiviazione sono stati distrutti. Questo errore viene restituito se il servizio Wireless Zero Configuration non ha inizializzato oggetti interni.<br/>                                                                                                                      |
| <dl> <dt>**FILE \_ DEGLI ERRORI NON \_ \_ TROVATO**</dt> </dl>   | Non è possibile trovare il file specificato. Questo errore viene restituito se il GUID nel membro **wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* non corrisponde ad alcuna interfaccia LAN wireless nel computer locale. <br/> |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl> | Un parametro non è corretto. Questo errore viene restituito se il *parametro pIntf* è **NULL.** Questo errore viene restituito se il **membro wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta *il parametro pIntf* è **NULL.** <br/>                            |
| <dl> <dt>**STATO \_ RPC**</dt> </dl>               | Vari codici di errore.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il **membro wszGuid** della struttura [**INTF \_ ENTRY**](intf-entry.md) a cui punta il *parametro pIntf* deve contenere un GUID di interfaccia per un'interfaccia LAN wireless. È possibile recuperare un elenco di interfacce LAN wireless chiamando la [**funzione WZCEnumInterfaces.**](wzcenuminterfaces.md)

> [!Note]  
> Il file *di intestazione Wzcsapi.h* e il file della libreria di importazione *Wzcsapi.lib* non sono disponibili in Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                         |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**VOCE \_ INTF**](intf-entry.md)
</dt> </dl>

 

 




