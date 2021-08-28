---
title: IWMPControls.isAvailable (VB e C )
description: La proprietà isAvailable (il metodo get isAvailable in C\ ) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire \_ un'azione specificata.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls.isAvailable (VB e C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054849"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls.isAvailable (VB e C#)

La **proprietà isAvailable** (metodo **get \_ isAvailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parametri

*bstrItem*

Oggetto System.String che è uno dei valori seguenti.



| Valore           | Descrizione                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Individua se l'utente può impostare la **proprietà IWMPControls.currentItem.**                                                                                     |
| currentMarker   | Individua se l'utente può cercare un marcatore specifico.                                                                                                         |
| currentPosition | Individua se l'utente può cercare una posizione specifica nel file. Alcuni file non supportano la ricerca.                                                        |
| Fastforward     | Individua se il file supporta l'inoltro rapido e se tale funzionalità può essere richiamata. Molti tipi di file (e flussi live) non supportano fastForward. |
| fastReverse     | Individua se il file supporta fastReverse e se tale funzionalità può essere richiamata. Molti tipi di file (e flussi live) non supportano fastReverse.     |
| Avanti            | Individua se l'utente può cercare la voce successiva in una playlist.                                                                                              |
| Sospendi           | Individua se il **metodo IWMPControls.pause** è disponibile.                                                                                                 |
| Giocare            | Individua se il **metodo IWMPControls.play** è disponibile.                                                                                                  |
| previous        | Individua se l'utente può cercare la voce precedente in una playlist.                                                                                          |
| step            | Individua se il **metodo IWMPControls2.step** è disponibile durante la riproduzione.                                                                                 |
| stop            | Individua se il **metodo IWMPControls.stop** è disponibile.                                                                                                  |



 

## <a name="property-value"></a>Valore della proprietà

**System.Boolean**

Valore **System.Boolean che** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

## <a name="remarks"></a>Commenti

**IWMPControls.isAvailable** è una proprietà in Visual Basic che accetta un parametro. In C# viene definito metodo **IWMPControls.get \_ isAvailable.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata la proprietà **isAvailable** (metodo **get \_ isAvailable** in C#) per verificare che l'elemento multimediale corrente supporti la **proprietà currentPosition.** **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls.pause (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2.step (VB e C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





