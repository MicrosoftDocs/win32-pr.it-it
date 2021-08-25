---
title: Metodo add IWMPMediaCollection
description: Il metodo add aggiunge un nuovo elemento multimediale o una nuova playlist alla libreria. | Metodo add IWMPMediaCollection
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Metodo add Windows Media Player
- Metodo add Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player , metodo add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861164"
---
# <a name="iwmpmediacollectionadd-method"></a>Metodo IWMPMediaCollection::add

Il **metodo add** aggiunge un nuovo elemento multimediale o una nuova playlist alla libreria.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* \[ Pollici\]
</dt> <dd>

**System.String che rappresenta** l'URL che specifica il percorso dell'elemento multimediale o della playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPMedia** per l'elemento o la playlist aggiunta.

## <a name="remarks"></a>Commenti

Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato un percorso. Questo metodo non sposta o modifica il file. Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità degli elementi multimediali prima dell'aggiunta alla libreria.

Questo metodo accetta file di playlist sia statici che automatici. Il **metodo IWMPPlaylistCollection.importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.

Prima di chiamare questo metodo, è necessario avere accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono aggiunti tre oggetti multimediali all Windows Media Player raccolta di supporti. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.remove (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.importPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





