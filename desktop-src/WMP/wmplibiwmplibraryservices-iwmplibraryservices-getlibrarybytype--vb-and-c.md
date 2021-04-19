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
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332411"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Metodo IWMPLibraryServices:: getLibraryByType

Il metodo **getLibraryByType** restituisce un'interfaccia **IWMPLibrary** che rappresenta la libreria con il tipo e l'indice specificati.

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

*wmplt* \[ in\]
</dt> <dd>

Valore dell'enumerazione **wmplib. WMPLibraryType** che specifica il tipo di libreria da recuperare.

</dd> <dt>

*lIndex* \[ in\]
</dt> <dd>

**System. Int32** che rappresenta l'indice della libreria da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPLibrary** per la libreria restituita.

## <a name="remarks"></a>Commenti

Esiste una sola libreria locale e le librerie di dischi sono disponibili solo sui CD di dati e i DVD che contengono contenuto multimediale.

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

 

 





