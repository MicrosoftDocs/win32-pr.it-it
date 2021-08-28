---
title: IWMPNetwork lostPackets - proprietà
description: La proprietà lostPackets ottiene il numero di pacchetti persi.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- Proprietà lostPackets Windows Media Player
- Proprietà lostPackets Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player proprietà , lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a60c85920d647f99ed8ba8478da51183c3ba63efa733c0bc627c16b040b70965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745912"
---
# <a name="iwmpnetworklostpackets-property"></a>Proprietà IWMPNetwork::lostPackets

La **proprietà lostPackets** ottiene il numero di pacchetti persi.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il numero di pacchetti persi.

## <a name="remarks"></a>Commenti

Questa proprietà include solo i pacchetti multimediali di streaming e restituirà zero quando si usa il protocollo HTTP, senza perdita di dati.

I pacchetti possono essere persi per diversi motivi, ad esempio il tipo e la qualità della connessione di rete.

Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero. Il valore non viene reimpostato se la riproduzione è sospesa. Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato usando la **proprietà AxWindowsMediaPlayer.URL.**

## <a name="examples"></a>Esempio

L'esempio di codice seguente **usa lostPackets** per visualizzare il numero totale di pacchetti persi durante la riproduzione. Le informazioni vengono visualizzate in un'etichetta quando l'utente fa clic su un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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

[**AxWindowsMediaPlayer.URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





