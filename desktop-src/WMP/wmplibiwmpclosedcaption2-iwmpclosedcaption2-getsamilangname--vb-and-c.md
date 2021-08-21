---
title: Metodo IWMPClosedCaption2 getSAMILangName
description: Il metodo getSAMILangName restituisce il nome di una lingua supportata dal file SAMI corrente.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Metodo getSAMILangName Windows Media Player
- Metodo getSAMILangName Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player metodo , getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99941c7c8c62480ea13572b22083a2d64bda9924cdf3d26200dbc9ac6ba9bdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930304"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>Metodo IWMPClosedCaption2::getSAMILangName

Il **metodo getSAMILangName** restituisce il nome di una lingua supportata dal file SAMI corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*nIndex* \[ Pollici\]
</dt> <dd>

**System.Int32** che rappresenta l'indice in base zero del nome della lingua da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System.String** che rappresenta il nome della lingua come specificato nel file SAMI.

## <a name="remarks"></a>Commenti

Le lingue in un file SAMI vengono indicizzate nell'ordine indicato nel file, a partire da zero.

Questo metodo restituisce una stringa di lunghezza zero ("") a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer.openState è uguale a 13).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





