---
title: IWMPMediaCollection Add (metodo)
description: Il metodo Add aggiunge un nuovo elemento multimediale o una playlist alla raccolta. | IWMPMediaCollection Add (metodo)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Aggiungi metodo Windows Media Player
- aggiungere il metodo Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, Aggiungi metodo
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
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324364"
---
# <a name="iwmpmediacollectionadd-method"></a>Metodo IWMPMediaCollection:: Add

Il metodo **Add** aggiunge un nuovo elemento multimediale o una playlist alla raccolta.

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

*bstrURL* \[ in\]
</dt> <dd>

**System. String** che rappresenta l'URL che specifica la posizione dell'elemento multimediale o della playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPMedia** per l'elemento o la playlist aggiunta.

## <a name="remarks"></a>Commenti

Questo metodo carica un elemento multimediale o una playlist esistente nella libreria, dato un percorso. Questo metodo non sposta o modifica il file. Questo metodo ha esito negativo se viene specificato un percorso locale non valido, ma non viene verificata la validità degli elementi multimediali prima che vengano aggiunti alla libreria.

Questo metodo accetta sia i file di playlist statici che quelli automatici. Il metodo **IWMPPlaylistCollection. importPlaylist** può essere usato anche per aggiungere una playlist statica alla libreria.

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente vengono aggiunti tre oggetti multimediali alla raccolta di supporti Windows Media Player. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. Remove (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





