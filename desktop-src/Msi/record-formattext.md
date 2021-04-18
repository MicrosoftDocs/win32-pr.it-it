---
description: Il metodo FormatText dell'oggetto record formatta i campi in base al modello nel campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Metodo record. FormatText
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
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330924"
---
# <a name="recordformattext-method"></a>Metodo record. FormatText

Il metodo **FormatText** dell'oggetto [**record**](record-object.md) formatta i campi in base al modello nel campo 0.

## <a name="syntax"></a>Sintassi


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **FormatText** segue la funzionalità della funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) se a **MsiFormatRecord** è stato passato un handle di programma di installazione null come primo parametro. Di conseguenza, vengono elaborati solo i parametri dei campi di record e le proprietà non sono disponibili per la sostituzione.

Ad esempio, una stringa come "formattare questo campo: \[ 1 \] , formattare questa proprietà: \[ Property \] " viene risolta in "formattare questo campo: valore dal campo 1, formattare questa proprietà: \[ Property \] ".

I parametri da [formattare](formatted.md) sono racchiusi tra parentesi quadre \[ ... \] . È possibile eseguire l'iterazione delle parentesi quadre perché le sostituzioni vengono risolte dalla parte interna.

Se una parte della stringa è racchiusa tra parentesi graffe {} e non contiene parentesi quadre, viene lasciata invariata, incluse le parentesi graffe.

Si noti che nel caso di [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md), **FormatText** supporta solo un set limitato di proprietà, ovvero le proprietà CustomActionData e ProductCode. Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
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

 

 




