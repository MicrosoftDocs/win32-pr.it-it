---
title: Proprietà maxBandwidth di IWMPNetwork
description: La proprietà maxBandwidth Ottiene o imposta la larghezza di banda massima consentita.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Finestra delle proprietà di maxBandwidth Media Player
- Proprietà di maxBandwidth Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329911"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>Proprietà IWMPNetwork:: maxBandwidth

La proprietà **maxBandwidth** Ottiene o imposta la larghezza di banda massima consentita.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta la larghezza di banda massima.

## <a name="remarks"></a>Commenti

Questa proprietà non ha un valore predefinito. Il valore può essere specificato durante la riproduzione di Windows Media Player, ma la modifica non verrà applicata fino a quando l'elemento multimediale corrente non viene rilasciato aprendone un altro o chiamando **AxWindowsMediaPlayer. Close**. Windows Media Player tenta di ottenere la massima larghezza di banda possibile. Non verrà eseguita alcuna riduzione intenzionale della larghezza di banda a meno che questo valore non sia impostato.

Questa impostazione è utile per ridurre la quantità di larghezza di banda usata, in particolare nel caso di un flusso a più velocità in bit (MBR). Un flusso MBR contiene più flussi con velocità in bit diverse. In alcuni casi, può essere utile usare un flusso con una velocità in bit inferiore a quella richiesta dal client. In questo caso, se si specifica una velocità in bit più bassa con la proprietà **IWMPNetwork. maxBandwidth** , verrà selezionato un flusso a velocità in bit inferiore. Ad esempio, un flusso MBR può includere flussi codificati a 20 kilobit al secondo (Kbps), 37 kbps e 200 Kbps. Se si usa **IWMPNetwork. maxBandwidth** per specificare una velocità in bit di 50.000 (50 Kbps), si selezionerà il flusso 37 Kbps anziché il flusso a 200 Kbps.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AxWindowsMediaPlayer. Close (VB e C#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





