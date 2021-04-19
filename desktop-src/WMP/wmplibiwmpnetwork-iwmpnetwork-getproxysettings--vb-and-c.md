---
title: Metodo IWMPNetwork getProxySettings
description: Il metodo getProxySettings restituisce informazioni sulle impostazioni proxy per un protocollo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Metodo getProxySettings Windows Media Player
- Metodo getProxySettings Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxySettings
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
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329913"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>Metodo IWMPNetwork:: getProxySettings

Il metodo **getProxySettings** restituisce informazioni sulle impostazioni proxy per un protocollo.

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

*bstrProtocol* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. Int32** che corrisponde a uno dei valori seguenti.



| Valore | Descrizione                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Non è in uso un server proxy.                                                |
| 1     | Vengono usate le impostazioni proxy per il browser corrente (valido solo per HTTP). |
| 2     | Sono in uso le impostazioni proxy specificate manualmente.                            |
| 3     | Le impostazioni proxy vengono rilevate automaticamente.                                      |



 

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato **getProxySettings** per visualizzare un messaggio, che fornisce informazioni sulle impostazioni proxy correnti del lettore, in un'etichetta. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





