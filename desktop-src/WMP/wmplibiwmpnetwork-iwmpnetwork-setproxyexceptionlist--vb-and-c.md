---
title: Metodo IWMPNetwork setProxyExceptionList
description: Il metodo setProxyExceptionList specifica l'elenco di eccezioni proxy. | Metodo IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- Metodo setProxyExceptionList Windows Media Player
- Metodo setProxyExceptionList Windows Media Player, interfaccia IWMPNetwork
- Metodo setProxyExceptionList dell'Windows Media Player IWMPNetwork
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddfd3ce8495c02fc6ae352f918349ff7174afb99e69d9e1ba8aa19c45d1a49d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745763"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a>Metodo IWMPNetwork::setProxyExceptionList

Il **metodo setProxyExceptionList** specifica l'elenco di eccezioni proxy.

## <a name="syntax"></a>Sintassi


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrProtocol* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome del protocollo. Per un elenco dei protocolli supportati, vedere [Protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> <dt>

*pbstrExceptionList* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che è un elenco delimitato da punti e virgola di host per cui il server proxy viene ignorato. Gli spazi iniziali e finali non devono essere presenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Si tratta di un elenco di computer, domini e/o indirizzi che ignorano il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.

Il \* carattere può essere usato come carattere jolly per elencare le voci. Ad esempio, .com corrisponderebbe a tutti gli host nel dominio com, mentre 67. corrisponderebbe a tutti gli host nella \* subnet A di classe \* 67.

Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork.getProxySettings non** sia 2 (usare le impostazioni manuali).

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene utilizzato **setProxyExceptionList** per specificare un elenco di host per cui il server proxy viene ignorato quando si usa il protocollo MMS. Il nuovo elenco viene recuperato da una casella di testo quando si fa clic su un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

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

[**IWMPNetwork.getProxyExceptionList (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork.getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





