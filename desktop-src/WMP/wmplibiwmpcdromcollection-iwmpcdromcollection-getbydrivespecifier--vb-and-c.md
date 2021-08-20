---
title: Metodo IWMPCdromCollection getByDriveSpecifier
description: Il metodo getByDriveSpecifier restituisce un'interfaccia IWMPCdrom associata a una lettera di unità specifica.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- Metodo getByDriveSpecifier Windows Media Player
- Metodo getByDriveSpecifier Windows Media Player, interfaccia IWMPCdromCollection
- Interfaccia IWMPCdromCollection Windows Media Player , metodo getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9937694234fe7e46fe9b98d83357da19abf18f8d14e83794587f6f2050b0019b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116219"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>Metodo IWMPCdromCollection::getByDriveSpecifier

Il **metodo getByDriveSpecifier** restituisce **un'interfaccia IWMPCdrom** associata a una lettera di unità specifica.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrDriveSpecifier* \[ Pollici\]
</dt> <dd>

**System.String che rappresenta** la lettera di unità seguita da due punti (":").

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPCdrom.**

## <a name="remarks"></a>Commenti

Le lettere di unità devono essere fornite nel formato *X*:, dove *X* rappresenta la lettera di unità.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

L'esempio seguente usa **getByDriveSpecifier** per ottenere **l'interfaccia IWMPCdrom** che corrisponde a una lettera di unità fornita dall'utente in una casella di testo. Il **metodo IWMPCdrom.eject** viene quindi chiamato per estrarre l'unità specificata. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom.eject (VB e C#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





