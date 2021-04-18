---
description: La proprietà FeatureState è lo stato di installazione della funzionalità per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryFeatureStateEx con ProductCode, UserSid e Context dell'oggetto. L'ID funzionalità viene fornito come parametro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Metodo Product. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326984"
---
# <a name="productfeaturestate-method"></a>Metodo Product. FeatureState

La proprietà **FeatureState** è lo stato di installazione della funzionalità per l'istanza di questo prodotto.

Questa proprietà chiama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)con *ProductCode*, *UserSID* e *context* dell'oggetto. L'ID funzionalità viene fornito come parametro.

## <a name="syntax"></a>Sintassi


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FeatureId* 
</dt> <dd>

ID funzionalità visualizzato nella colonna funzionalità della [tabella delle funzionalità](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come **DWORD**.



| State                    | Significato                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ annunciata | Questa funzionalità è annunciata.                  |
| INSTALLSTATE \_ locale      | La funzionalità viene installata localmente.            |
| \_origine InstallState     | La funzionalità è installata per l'esecuzione dall'origine. |



 

Se la chiamata ha esito negativo, la proprietà contiene un codice di errore di [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Errore                     | Significato                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE di \_ accesso \_ negato     | Il processo chiamante deve disporre di privilegi amministrativi per ottenere informazioni relative a un prodotto installato per un utente diverso dall'utente corrente. |
| ERRORE \_ configurazione errata \_ | I dati di configurazione sono danneggiati.                                                                                                         |
| ERRORE \_ parametro non valido \_ | Un parametro non valido è stato passato alla funzione.                                                                                           |
| ERRORE \_ riuscito            | La funzione è stata completata correttamente.                                                                                                       |
| \_funzionalità sconosciuta di errore \_   | L'ID funzionalità non identifica una funzionalità nota.                                                                                          |
| ERRORE \_ \_ prodotto sconosciuto   | Il codice prodotto non identifica un prodotto noto.                                                                                        |
| \_funzione Error \_ non riuscita   | Errore interno imprevisto.                                                                                                            |



 

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

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




