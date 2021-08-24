---
title: Metodo IWMPClosedCaption2 getSAMIStyleName
description: Il metodo getSAMIStyleName restituisce il nome di uno stile supportato dal file SAMI corrente.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- Metodo getSAMIStyleName Windows Media Player
- Metodo getSAMIStyleName Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player metodo , getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd599370afb9029a481fbae33264796232e4f129c1a5da0d2658452b785a870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031351"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>Metodo IWMPClosedCaption2::getSAMIStyleName

Il **metodo getSAMIStyleName** restituisce il nome di uno stile supportato dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*nIndex* \[ Pollici\]
</dt> <dd>

Oggetto **System.Int32** che rappresenta l'indice in base zero del nome dello stile da recuperare

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto **System.String** che rappresenta il nome dello stile specificato nel file SAMI.

## <a name="remarks"></a>Commenti

Gli stili in un file SAMI vengono indicizzati nell'ordine indicato nel file, a partire da zero.

Questo metodo restituisce una stringa di lunghezza zero ("") a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer.openState è uguale a 13).

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

[**IWMPClosedCaption.SAMIStyle (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





