---
description: Ottiene i parametri di configurazione avvio EAPOL per l'interfaccia LAN wireless specificata.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Funzione WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317105"
---
# <a name="wzceapolgetinterfaceparams-function"></a>WZCEapolGetInterfaceParams (funzione)

\[**WZCEapolGetInterfaceParams** non è più supportato a partire da Windows Vista e windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

La funzione **WZCEapolGetInterfaceParams** ottiene i parametri di configurazione di avvio EAPOL per l'interfaccia LAN wireless specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrvAddr* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome del computer in cui eseguire questa funzione. Se questo parametro è **null**, il servizio di configurazione zero senza fili viene chiamato sul computer locale.

Se il parametro *pSrvAddr* specificato è un computer remoto, il computer remoto deve supportare le chiamate RPC remote.

</dd> <dt>

*pwszGuid* \[ in\]
</dt> <dd>

GUID dell'interfaccia per cui recuperare i dati.

</dd> <dt>

*dwSizeOfSSID* \[ in\]
</dt> <dd>

Dimensioni dell'identificatore di rete per cui devono essere recuperati i dati.

</dd> <dt>

*pbSSID* \[ in\]
</dt> <dd>

Puntatore all'identificatore di rete per il quale devono essere recuperati i dati.

</dd> <dt>

*pIntfParams* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**avvio EAPOL \_ INTF \_ params**](eapol-intf-params.md) che contiene i parametri dell'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ l'errore se l'operazione viene completata correttamente; in caso contrario, restituisce uno dei codici di errore di sistema di Windows.

## <a name="remarks"></a>Commenti

Se **WZCEapolGetInterfaceParams** restituisce Error \_ Success, il chiamante deve chiamare [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) per rilasciare i buffer interni allocati per i dati restituiti una volta che queste informazioni non sono più necessarie.

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

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
