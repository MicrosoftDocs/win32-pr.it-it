---
title: Metodo IWMPNetwork setProxyName
description: Il metodo setProxyName specifica il nome del server proxy da usare. | Metodo IWMPNetwork setProxyName
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- Metodo setProxyName Windows Media Player
- Metodo setProxyName Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo setProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4525b3933f0929413a2719e1338083b00b9995a4ba39085f5787c6feca9931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568716"
---
# <a name="iwmpnetworksetproxyname-method"></a>Metodo IWMPNetwork::setProxyName

Il **metodo setProxyName** specifica il nome del server proxy da usare.

## <a name="syntax"></a>Sintassi


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrProtocol* \[ Pollici\]
</dt> <dd>

**System.String che** rappresenta il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati.](supported-protocols-and-file-types.md)

</dd> <dt>

*bstrProxyName* \[ Pollici\]
</dt> <dd>

**System.String** che rappresenta il nome del server proxy da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork.getProxySettings non** sia 2 (usare le impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente **viene utilizzato setProxyName** per specificare il nome del server proxy Windows Media Player per il protocollo MMS. Il nuovo nome viene recuperato da una casella di testo quando si fa clic su un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
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

[**IWMPNetwork.getProxyName (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





