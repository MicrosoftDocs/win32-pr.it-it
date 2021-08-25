---
title: Metodo CdromCollection.getByDriveSpecifier
description: Il metodo getByDriveSpecifier recupera l'oggetto Cdrom associato a una lettera di unità specifica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Metodo getByDriveSpecifier Windows Media Player
- Metodo getByDriveSpecifier Windows Media Player , classe CdromCollection
- Classe CdromCollection Windows Media Player metodo , getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864091"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Metodo CdromCollection.getByDriveSpecifier

Il **metodo getByDriveSpecifier** recupera l'oggetto **Cdrom** associato a una lettera di unità specifica.

## <a name="syntax"></a>Sintassi


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*driveSpecifier* \[ Pollici\]
</dt> <dd>

**Stringa** contenente la lettera di unità seguita da due punti (":").

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Cdrom.**

## <a name="remarks"></a>Commenti

Le lettere di unità devono essere fornite nel formato *X*:, dove *X* rappresenta la lettera di unità.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato CdromCollection*. **getByDriveSpecifier per** recuperare **l'oggetto Cdrom** che corrisponde a una lettera di unità fornita dall'utente. È stato creato un elemento di testo HTML, con NAME = "MyText", per l'input dell'utente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdrom.eject**](cdrom-eject.md)
</dt> <dt>

[**Oggetto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





