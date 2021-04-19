---
title: Metodo IWMPNetwork getProxyExceptionList
description: Il metodo getProxyExceptionList restituisce l'elenco di eccezioni del proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- Metodo getProxyExceptionList Windows Media Player
- Metodo getProxyExceptionList Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324717"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a>Metodo IWMPNetwork:: getProxyExceptionList

Il metodo **getProxyExceptionList** restituisce l'elenco di eccezioni del proxy.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrProtocol* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome del protocollo. Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato. Il valore è significativo solo quando **IWMPNetwork. getProxySettings** restituisce un valore pari a 2 (usare impostazioni manuali).

## <a name="remarks"></a>Commenti

Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.

Il \* carattere può essere usato come carattere jolly per elencare le voci. Ad esempio, \* . com corrisponde a tutti gli host nel dominio com, mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.

Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato **getProxyExceptionList** per visualizzare se Windows Media Player è impostato in modo da ignorare il server proxy per gli indirizzi locali. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
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

[**IWMPNetwork. getProxySettings (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyExceptionList (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





