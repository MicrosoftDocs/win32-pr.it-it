---
description: La proprietà FeatureState è lo stato di installazione della funzionalità per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryFeatureStateEx, con ProductCode, UserSid e Context dell'oggetto. L'ID funzionalità viene fornito come parametro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Metodo Product.FeatureState
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
ms.openlocfilehash: 484b8f7f3094cf5bca2cb9d03941d68619995ba98de08e2845c3717439709e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129051"
---
# <a name="productfeaturestate-method"></a>Metodo Product.FeatureState

La **proprietà FeatureState** è lo stato di installazione della funzionalità per l'istanza di questo prodotto.

Questa proprietà chiama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)con *ProductCode,* *UserSid* *e Context* dell'oggetto. L'ID funzionalità viene fornito come parametro.

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

ID funzionalità visualizzato nella colonna Funzionalità della [tabella delle funzionalità](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come **valore DWORD**.



| State                    | Significato                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ ANNUNCIATO | Questa funzionalità è annunciata.                  |
| INSTALLSTATE \_ LOCAL      | La funzionalità viene installata in locale.            |
| ORIGINE \_ INSTALLSTATE     | La funzionalità viene installata per l'esecuzione dall'origine. |



 

Se la chiamata ha esito negativo, la proprietà contiene un codice di errore [**da MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Errore                     | Significato                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ DI ACCESSO \_ NEGATO     | Il processo chiamante deve avere privilegi amministrativi per ottenere informazioni per un prodotto installato per un utente diverso dall'utente corrente. |
| ERRORE \_ CONFIGURAZIONE \_ NON VALIDA | I dati di configurazione sono danneggiati.                                                                                                         |
| ERRORE \_ PARAMETRO NON \_ VALIDO | Alla funzione è stato passato un parametro non valido.                                                                                           |
| ERRORE \_ RIUSCITO            | La funzione è stata completata correttamente.                                                                                                       |
| FUNZIONALITÀ \_ DI ERRORE \_ SCONOSCIUTA   | L'ID funzionalità non identifica una funzionalità nota.                                                                                          |
| ERRORE \_ PRODOTTO \_ SCONOSCIUTO   | Il codice prodotto non identifica un prodotto noto.                                                                                        |
| FUNZIONE \_ ERROR \_ NON RIUSCITA   | Errore interno imprevisto.                                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




