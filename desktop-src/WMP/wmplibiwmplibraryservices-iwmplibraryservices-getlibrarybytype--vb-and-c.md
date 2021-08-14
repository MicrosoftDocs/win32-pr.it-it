---
title: Metodo IWMPLibraryServices getLibraryByType
description: Il metodo getLibraryByType restituisce un'interfaccia IWMPLibrary che rappresenta la libreria con il tipo e l'indice specificati.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- Metodo getLibraryByType Windows Media Player
- Metodo getLibraryByType Windows Media Player, interfaccia IWMPLibraryServices
- Interfaccia IWMPLibraryServices Windows Media Player, metodo getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f83d74c8c03f8b08936c3693c77e211cd87a8b42c2d020c26ee5133406a2a042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746209"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Metodo IWMPLibraryServices::getLibraryByType

Il **metodo getLibraryByType** restituisce **un'interfaccia IWMPLibrary** che rappresenta la libreria con il tipo e l'indice specificati.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*wmplt* \[ Pollici\]
</dt> <dd>

Valore **dell'enumerazione WMPLib.WMPLibraryType** che specifica il tipo di libreria da recuperare.

</dd> <dt>

*lIndex* \[ Pollici\]
</dt> <dd>

**System.Int32** che rappresenta l'indice della libreria da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPLibrary** per la libreria restituita.

## <a name="remarks"></a>Commenti

Esiste una sola libreria locale e le librerie dei dischi sono disponibili solo per i CD di dati e i DVD che contengono contenuto multimediale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





