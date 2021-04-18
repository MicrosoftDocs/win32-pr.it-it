---
title: IWMPControls. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. disavailable (VB e C) Windows Media Player
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
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328213"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls. disavailable (VB e C#)

La proprietà **disavailable** (il metodo **get \_ disavailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.


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

System. String che corrisponde a uno dei valori seguenti.



| Valore           | Descrizione                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Individua se l'utente può impostare la proprietà **IWMPControls. CurrentItem** .                                                                                     |
| currentMarker   | Individua se l'utente può cercare un marcatore specifico.                                                                                                         |
| currentPosition | Individua se l'utente può eseguire la ricerca in una posizione specifica nel file. Alcuni file non supportano la ricerca.                                                        |
| fastForward     | Rileva se il file supporta l'avanzamento rapido e se tale funzionalità può essere richiamata. Molti tipi di file (e flussi live) non supportano fastForward. |
| fastReverse     | Rileva se il file supporta fastReverse e se tale funzionalità può essere richiamata. Molti tipi di file (e flussi live) non supportano fastReverse.     |
| Avanti            | Individua se l'utente può cercare la voce successiva in una playlist.                                                                                              |
| Sospendi           | Individua se è disponibile il metodo **IWMPControls. pause** .                                                                                                 |
| Play            | Rileva se il metodo **IWMPControls. Play** è disponibile.                                                                                                  |
| previous        | Individua se l'utente può cercare la voce precedente in una playlist.                                                                                          |
| step            | Rileva se il metodo **IWMPControls2. Step** è disponibile durante la riproduzione.                                                                                 |
| stop            | Rileva se il metodo **IWMPControls. Stop** è disponibile.                                                                                                  |



 

## <a name="property-value"></a>Valore della proprietà

**System.Boolean**

**System. Boolean** che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.

## <a name="remarks"></a>Commenti

**IWMPControls. disavailable** è una proprietà in Visual Basic che accetta un parametro. In C# viene indicato come il metodo **IWMPControls. Get \_ unavailable** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata **la proprietà IsValid** (il metodo **get \_ disavailable** in C#) per verificare che l'elemento multimediale corrente supporti la proprietà **currentPosition** . L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls. pause (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. Step (VB e C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





