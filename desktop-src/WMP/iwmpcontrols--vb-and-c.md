---
title: Interfaccia IWMPControls (VB e C) (WMP. h)
description: Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause. l'interfaccia IWMPControls espone le proprietà seguenti.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Interfaccia IWMPControls (VB e C) Windows Media Player
- Interfaccia IWMPControls (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328216"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Interfaccia IWMPControls (VB e C#)

Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause.

L'interfaccia **IWMPControls** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPControls (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPControls (VB e C#)** presenta questi metodi.



| Metodo                                                                       | Descrizione                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**fastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Avvia la riproduzione veloce dell'elemento multimediale nella direzione in avanti.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Avvia la riproduzione veloce dell'elemento multimediale nella direzione inversa.<br/>                     |
| [**prossimo**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Imposta l'elemento successivo nella playlist come elemento corrente.<br/>                          |
| [**pause**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Sospende la riproduzione dell'elemento multimediale.<br/>                                               |
| [**Play**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Inizia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Riproduce l'elemento multimediale specificato.<br/>                                                  |
| [**precedente**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Imposta l'elemento precedente nella playlist come elemento corrente.<br/>                      |
| [**arrestare**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Interrompe la riproduzione dell'elemento multimediale.<br/>                                                |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPControls (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                                    | Tipo di accesso           | Descrizione                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**currentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'elemento multimediale corrente in una playlist.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il numero dell'indicatore corrente.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene la posizione corrente nell'elemento multimediale come **System. String**.<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Sola lettura<br/>  | Ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. In C# si tratta del metodo **get \_ unavailable** .<br/> |



 

Ottenere un'interfaccia **IWMPControls** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





