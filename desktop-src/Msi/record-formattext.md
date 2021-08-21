---
description: Il metodo FormatText dell'oggetto Record formatta i campi in base al modello nel campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Metodo Record.FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 28170a4d92f656dcd12863eca5c003ccb851772f42de375e8f5f1b61a768ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626981"
---
# <a name="recordformattext-method"></a>Metodo Record.FormatText

Il **metodo FormatText** dell'oggetto [**Record**](record-object.md) formatta i campi in base al modello nel campo 0.

## <a name="syntax"></a>Sintassi


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo FormatText** segue la funzionalità della funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) se **a MsiFormatRecord** è stato passato un handle di installazione Null come primo parametro. Di conseguenza, vengono elaborati solo i parametri del campo record e le proprietà non sono disponibili per la sostituzione.

Ad esempio, una stringa come "format this field: 1 , format this property: property " viene risolta in \[ \] \[ \] "format this field: value from field 1, format this \[ property: \] property".

I parametri da [formattare sono](formatted.md) racchiusi tra parentesi quadre... \[ \] . Le parentesi quadre possono essere iterate perché le sostituzioni vengono risolte dall'interno all'esterno.

Se una parte della stringa è racchiusa tra parentesi graffe { } e non contiene parentesi quadre, viene lasciata invariata, incluse le parentesi graffe.

Si noti che nel caso di azioni [personalizzate](deferred-execution-custom-actions.md)di esecuzione posticipata, **FormatText** supporta solo un set limitato di proprietà: le proprietà CustomActionData e ProductCode. Per altre informazioni, vedere [Recupero di informazioni sul contesto per le azioni personalizzate di esecuzione posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Formattato](formatted.md)
</dt> <dt>

[Tipi di dati delle colonne](column-data-types.md)
</dt> </dl>

 

 




