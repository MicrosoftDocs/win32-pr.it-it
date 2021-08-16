---
description: La proprietà ComponentState è lo stato di installazione del componente per l'istanza di questo prodotto. Questa proprietà chiama MsiQueryComponentState, con ProductCode, UserSid e Context dell'oggetto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Metodo Product.ComponentState
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
ms.openlocfilehash: d2bc9c5c1f5325dc631f8866ba1a8c7d88ce18d624a2974974f4692bf4f7b067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376780"
---
# <a name="productcomponentstate-method"></a>Metodo Product.ComponentState

La **proprietà ComponentState** è lo stato di installazione del componente per l'istanza di questo prodotto.

Questa proprietà chiama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)con ProductCode, UserSid e Context dell'oggetto. Il GUID dell'ID componente viene fornito come parametro.

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

GUID del codice componente del componente trovato nella colonna ComponentID della [tabella Component](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la proprietà contiene il valore come **valore DWORD**.



| State                | Significato                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ LOCAL  | Il componente viene installato in locale.                |
| ORIGINE \_ INSTALLSTATE | Il componente viene installato per l'esecuzione dall'origine. |



 

Se la chiamata ha esito negativo, la proprietà contiene un codice di errore [**da MsiQueryComponentState.**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)



| Errore                     | Significato                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ DI ACCESSO \_ NEGATO     | Il processo chiamante deve avere privilegi amministrativi per ottenere informazioni per un utente diverso dall'utente corrente. |
| ERRORE \_ CONFIGURAZIONE \_ NON VALIDA | I dati di configurazione sono danneggiati.                                                                                 |
| ERRORE \_ PARAMETRO NON \_ VALIDO | Alla funzione è stato passato un parametro non valido.                                                                   |
| ERRORE \_ RIUSCITO            | La funzione è stata completata correttamente.                                                                               |
| ERRORE \_ COMPONENTE \_ SCONOSCIUTO | L'ID componente non identifica un componente noto.                                                              |
| ERRORE \_ PRODOTTO \_ SCONOSCIUTO   | Il codice prodotto non identifica un prodotto noto.                                                                |
| FUNZIONE \_ ERROR \_ NON RIUSCITA   | Errore interno imprevisto.                                                                                    |



 

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

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




