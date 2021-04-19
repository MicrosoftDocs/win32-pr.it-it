---
title: Metodo IWMPClosedCaption2 getSAMILangName
description: Il metodo getSAMILangName restituisce il nome di una lingua supportata dal file SAMI corrente.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- Metodo getSAMILangName Windows Media Player
- Metodo getSAMILangName Windows Media Player, interfaccia IWMPClosedCaption2
- Interfaccia IWMPClosedCaption2 Windows Media Player, metodo getSAMILangName
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
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332495"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>Metodo IWMPClosedCaption2:: getSAMILangName

Il metodo **getSAMILangName** restituisce il nome di una lingua supportata dal file Sami corrente.

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

*nIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice in base zero del nome del linguaggio da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**System. String** che rappresenta il nome del linguaggio come specificato nel file Sami.

## <a name="remarks"></a>Commenti

Le lingue in un file SAMI sono indicizzate nell'ordine indicato nel file, a partire da zero.

Questo metodo restituisce una stringa di lunghezza zero (""), a meno che non sia aperto un file multimediale digitale (AxWindowsMediaPlayer. openState è uguale a 13).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





