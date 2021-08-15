---
title: Metodo IWMPNetwork getProxySettings
description: Il metodo getProxySettings restituisce informazioni sulle impostazioni proxy per un protocollo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Metodo getProxySettings Windows Media Player
- Metodo getProxySettings Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player metodo , getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e69c990b01ed885b80c96e3e36ad28c2793baf618fea68b0e20006390c2adeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331641"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>Metodo IWMPNetwork::getProxySettings

Il **metodo getProxySettings** restituisce informazioni sulle impostazioni proxy per un protocollo.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrProtocol* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.Int32** che è uno dei valori seguenti.



| Valore | Descrizione                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Un server proxy non è in uso.                                                |
| 1     | Vengono usate le impostazioni proxy per il browser corrente (valide solo per HTTP). |
| 2     | Vengono usate le impostazioni proxy specificate manualmente.                            |
| 3     | Le impostazioni proxy vengono rilevate automaticamente.                                      |



 

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

## <a name="examples"></a>Esempio

L'esempio di codice seguente usa **getProxySettings** per visualizzare un messaggio, che fornisce informazioni sulle impostazioni proxy correnti di Player, in un'etichetta. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.setProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





