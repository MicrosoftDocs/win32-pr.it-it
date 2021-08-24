---
title: Metodo setDeleted IWMPMediaCollection
description: Il metodo setDeleted sposta l'elemento multimediale specificato nella cartella degli elementi eliminati. | Metodo setDeleted IWMPMediaCollection
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- Metodo setDeleted Windows Media Player
- Metodo setDeleted Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player , metodo setDeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516d6aab26659fa2bba57bd961671b4dca0f92d367d5d9bb1f048e8fd19eb2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505951"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>Metodo IWMPMediaCollection::setDeleted

Il `setDeleted` metodo sposta l'elemento multimediale specificato nella cartella degli elementi eliminati.

## <a name="syntax"></a>Sintassi


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pItem* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPMedia** per l'elemento da spostare.

</dd> <dt>

*varfIsDeleted* \[ Pollici\]
</dt> <dd>

Valore **System.Boolean** che specifica se l'elemento deve essere spostato nella cartella degli elementi eliminati. Questo valore deve sempre essere **true.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo non rimuove i file dal computer dell'utente, ma li sposta semplicemente nella cartella degli elementi eliminati.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente `setDeleted` viene utilizzato per spostare un particolare elemento multimediale nella cartella degli elementi eliminati. Il **metodo isDeleted** verifica innanzitutto se l'elemento è già stato eliminato. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





