---
title: AxWindowsMediaPlayer. newMedia, metodo
description: Il metodo newMedia restituisce un'interfaccia IWMPMedia per un nuovo elemento multimediale.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- Metodo newMedia Windows Media Player
- Metodo newMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329443"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>AxWindowsMediaPlayer. newMedia, metodo

Il metodo newMedia restituisce un'interfaccia IWMPMedia per un nuovo elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** che rappresenta l'URL del file multimediale digitale utilizzato per inizializzare il nuovo elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia WMPLib. IWMPMedia che rappresenta l'elemento multimediale appena creato.

## <a name="remarks"></a>Commenti

Il parametro *bstrURL* non deve essere una stringa di lunghezza zero ("") o null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





