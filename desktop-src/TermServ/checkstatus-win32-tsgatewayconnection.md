---
title: Metodo CheckStatus della classe Win32_TSGatewayConnection
description: Controlla lo stato di una connessione del server Gateway Desktop remoto (Gateway Desktop remoto) a un altro computer e determina se il computer di destinazione è configurato per il bilanciamento del carico.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CheckStatus
- Metodo CheckStatus Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301232"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a>Metodo CheckStatus della \_ classe TSGatewayConnection Win32

Controlla lo stato di una connessione del server Gateway Desktop remoto (Gateway Desktop remoto) a un altro computer e determina se il computer di destinazione è configurato per il bilanciamento del carico.

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nomeserver* \[ in\]
</dt> <dd>

Nome del server Gateway Desktop remoto di origine da cui viene verificata la connessione.

</dd> <dt>

*EndpointName* \[ in\]
</dt> <dd>

Nome del server di destinazione (l'endpoint) a cui viene effettuato il controllo dell'accesso dal server di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti possibili seguenti.

<dl> <dt>


</dt> <dd>

0

Lo stato della connessione è OK. L'endpoint è raggiungibile ed è configurato per il bilanciamento del carico.

</dd> <dt>


</dt> <dd>

1

Lo stato della connessione è sconosciuto. È probabile che si sia verificata un'eccezione.

</dd> <dt>


</dt> <dd>

0x80075c34

L'endpoint non è raggiungibile o non è configurato per il bilanciamento del carico.

</dd> <dt>


</dt> <dd>

0x80075c32

Si è verificato un errore di stato. L'endpoint è raggiungibile, ma il servizio di bilanciamento del carico RPC/HTTP (RPCHTTPLBS) non è stato avviato nel computer di destinazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> </dl>

 

