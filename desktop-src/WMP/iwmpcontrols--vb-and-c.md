---
title: Interfaccia IWMPControls (VB e C) (Wmp.h)
description: Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di trasporto di Windows Media Player, ad esempio Play, Stop e Pause. L'interfaccia IWMPControls espone le proprietà seguenti.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Interfaccia IWMPControls (VB e C) Windows Media Player
- Interfaccia IWMPControls (VB e C) Windows Media Player , descritta
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
ms.openlocfilehash: 1b96f79b8942935d9722bf38dbd1ae946b03d16496664b4c069552819785c1f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119310"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Interfaccia IWMPControls (VB e C#)

Consente di modificare la riproduzione di un elemento multimediale rappresentando i controlli di Windows Media Player, ad esempio Play, Stop e Pause.

**L'interfaccia IWMPControls** espone le proprietà seguenti.

## <a name="members"></a>Membri

**L'interfaccia IWMPControls (VB e C#)** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IWMPControls (VB e C#).**



| Metodo                                                                       | Descrizione                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Fastforward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Avvia la riproduzione rapida dell'elemento multimediale in avanti.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Avvia la riproduzione veloce dell'elemento multimediale nella direzione inversa.<br/>                     |
| [**prossimo**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Imposta l'elemento successivo nella playlist come elemento corrente.<br/>                          |
| [**Pausa**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Sospende la riproduzione dell'elemento multimediale.<br/>                                               |
| [**Giocare**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Avvia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Riproduce l'elemento multimediale specificato.<br/>                                                  |
| [**Precedente**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Imposta l'elemento precedente nella playlist come elemento corrente.<br/>                      |
| [**Fermare**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Arresta la riproduzione dell'elemento multimediale.<br/>                                                |



 

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IWMPControls (VB e C#).**



| Proprietà                                                                                                    | Tipo di accesso           | Descrizione                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l'elemento multimediale corrente in una playlist.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il numero del marcatore corrente.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene la posizione corrente nell'elemento multimediale come **oggetto System.String**.<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Sola lettura<br/>  | Ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata. In C# si tratta del **metodo get \_ isAvailable.**<br/> |



 

Ottenere **un'interfaccia IWMPControls** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





