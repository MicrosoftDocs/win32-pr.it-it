---
title: Metodo getSAMILangID IWMPClosedCaption2
description: Il metodo getSAMILangID restituisce l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Metodo getSAMILangID Windows Media Player
- Metodo getSAMILangID Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player metodo , getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0fc62222f98d6c056bb8ce9ffd328582a6764202bb8446617471d3f7cb4a5ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506431"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>Metodo IWMPClosedCaption2::getSAMILangID

Il **metodo getSAMILangID** restituisce l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*nIndex* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che rappresenta l'indice in base zero dell'LCID da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.Int32** che rappresenta l'LCID della lingua con l'indice specificato.

## <a name="remarks"></a>Commenti

Le lingue in un file SAMI vengono indicizzate nell'ordine indicato nel file, a partire da zero.

Questo metodo restituisce 0 a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer.openState è uguale a 13).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





