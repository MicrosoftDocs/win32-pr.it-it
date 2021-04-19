---
title: Cdromcollection. getByDriveSpecifier, metodo
description: Il metodo getByDriveSpecifier recupera l'oggetto cdrom associato a una lettera di unità specifica.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Metodo getByDriveSpecifier Windows Media Player
- Metodo getByDriveSpecifier Windows Media Player, classe cdromcollection
- Classe cdromcollection Windows Media Player, metodo getByDriveSpecifier
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
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333135"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Cdromcollection. getByDriveSpecifier, metodo

Il metodo **getByDriveSpecifier** recupera l'oggetto **CDROM** associato a una lettera di unità specifica.

## <a name="syntax"></a>Sintassi


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*driveSpecifier* \[ in\]
</dt> <dd>

**Stringa** contenente la lettera di unità seguita da un carattere due punti (":").

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **CDROM** .

## <a name="remarks"></a>Commenti

Le lettere di unità devono essere specificate nel formato *x*:, dove *x* rappresenta la lettera di unità.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *cdromcollection*. **getByDriveSpecifier** per recuperare l'oggetto **CDROM** che corrisponde a una lettera di unità fornita dall'utente. È stato creato un elemento di testo HTML, con nome = "testo", per l'input dell'utente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Cdrom. EJECT**](cdrom-eject.md)
</dt> <dt>

[**Oggetto cdromcollection**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





