---
description: La proprietà ComponentState è lo stato di installazione del componente per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryComponentState con ProductCode, UserSid e Context dell'oggetto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Metodo Product. ComponentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330283"
---
# <a name="productcomponentstate-method"></a>Metodo Product. ComponentState

La proprietà **ComponentState** è lo stato di installazione del componente per l'istanza di questo prodotto.

Questa proprietà chiama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)con ProductCode, UserSID e Context dell'oggetto. Il GUID dell'ID componente viene fornito come parametro.

## <a name="syntax"></a>Sintassi


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* 
</dt> <dd>

GUID del codice componente del componente, disponibile nella colonna ComponentID della tabella dei [componenti](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come **DWORD**.



| State                | Significato                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ locale  | Il componente viene installato localmente.                |
| \_origine InstallState | Il componente è installato per l'esecuzione dall'origine. |



 

Se la chiamata ha esito negativo, la proprietà contiene un codice di errore di [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Errore                     | Significato                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERRORE di \_ accesso \_ negato     | Il processo chiamante deve disporre di privilegi amministrativi per ottenere informazioni per un utente diverso dall'utente corrente. |
| ERRORE \_ configurazione errata \_ | I dati di configurazione sono danneggiati.                                                                                 |
| ERRORE \_ parametro non valido \_ | Un parametro non valido è stato passato alla funzione.                                                                   |
| ERRORE \_ riuscito            | La funzione è stata completata correttamente.                                                                               |
| ERRORE \_ \_ componente sconosciuto | L'ID componente non identifica un componente noto.                                                              |
| ERRORE \_ \_ prodotto sconosciuto   | Il codice prodotto non identifica un prodotto noto.                                                                |
| \_funzione Error \_ non riuscita   | Errore interno imprevisto.                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




