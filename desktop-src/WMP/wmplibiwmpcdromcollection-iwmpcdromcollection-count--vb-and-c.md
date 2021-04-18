---
title: IWMPCdromCollection-proprietà conteggio
description: La proprietà Count ottiene il numero di unità CD e DVD disponibili nel sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- conteggio delle proprietà di Windows Media Player
- Proprietà Count Media Player Windows, interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection Windows Media Player, proprietà Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329652"
---
# <a name="iwmpcdromcollectioncount-property"></a>Proprietà IWMPCdromCollection:: count

La proprietà **count** ottiene il numero di unità CD e DVD disponibili nel sistema.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero di unità disponibili.

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Le unità DVD sono conteggiate esattamente come le unità CD. Tuttavia, il controllo ActiveX di Windows Media Player supporta solo la funzionalità DVD per Windows XP o versione successiva. In genere, le unità DVD possono riprodurre supporti CD, ma le unità CD non possono riprodurre supporti DVD.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato Count per visualizzare il numero di unità CD e DVD disponibili in una finestra di messaggio. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





