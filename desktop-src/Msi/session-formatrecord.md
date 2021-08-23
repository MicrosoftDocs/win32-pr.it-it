---
description: Il metodo FormatRecord dell'oggetto Session restituisce una stringa formattata da un modello e da dati di record.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Metodo Session.FormatRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f58aabc0bd222b22ee74cb0b431ce8051ed6bad546d963160c922bd86dee2383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629151"
---
# <a name="sessionformatrecord-method"></a>Metodo Session.FormatRecord

Il **metodo FormatRecord** dell'oggetto [**Session**](session-object.md) restituisce una stringa formattata da un modello e da dati di record.

## <a name="syntax"></a>Sintassi


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Registrazione* 
</dt> <dd>

Oggetto **Record obbligatorio** contenente un modello e i dati da formattare. La stringa del modello deve essere impostata nel campo 0 seguito da eventuali parametri di dati a cui si fa riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo FormatRecord** usa il processo di formato seguente.

I parametri da [formattare](formatted.md) sono racchiusi tra parentesi \[ quadre. . \] . Le parentesi quadre possono essere itere perché le sostituzioni vengono risolte dall'interno all'esterno.

Se una parte della stringa è racchiusa tra parentesi graffe { } e non contiene parentesi quadre, la parte rimane invariata, incluse le parentesi graffe.

Se una parte della stringa è racchiusa tra parentesi graffe e contiene uno o più nomi di proprietà e se vengono trovate tutte le proprietà, il testo (con le sostituzioni risolte) viene visualizzato senza le parentesi graffe. Se una delle proprietà non viene trovata, tutto il testo tra parentesi graffe e le parentesi graffe stesse viene rimosso.

**Per formattare le stringhe usando il metodo FormatRecord**

1.  I parametri numerici vengono sostituiti sostituendo il marcatore con il valore del campo record corrispondente, con valori mancanti o Null che non producono testo.
2.  La stringa restituita viene elaborata sostituendo i parametri non di record con i valori corrispondenti, come illustrato nelle descrizioni seguenti.
    -   Se viene rilevata una sottostringa nel formato " propertyname ", viene sostituita \[ dal valore della proprietà \] .
    -   Se viene trovata una sottostringa nel formato " %environmentvariable ", il valore della variabile di ambiente \[ \] viene sostituito.
    -   Se viene trovata una sottostringa del formato \[ \# *filekey,* viene sostituita dal percorso completo del \] file, [](file-table.md)con il valore *filekey* usato come chiave nella tabella File . Il valore di filekey rimane vuoto e non viene sostituito da un percorso finché il programma di installazione non esegue l'azione \[ \#  \] [CostInitialize](costinitialize-action.md), [l'azione FileCost](filecost-action.md)e [l'azione CostFinalize](costfinalize-action.md). Il valore di \[ \# *filekey* \] dipende dallo stato di installazione del componente a cui appartiene il file. Se il componente viene eseguito dall'origine, il valore è il percorso del percorso di origine del file. Se il componente viene eseguito in locale, il valore è il percorso del percorso di destinazione del file dopo l'installazione. Se il componente è assente, il percorso è vuoto. Per altre informazioni sul controllo dello stato di installazione dei componenti, vedere [Controllo dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
    -   Se viene trovata una sottostringa del formato $componentkey, viene sostituita dalla directory di installazione del componente, con il valore \[  \] *componentkey* usato come chiave nella [tabella Component](component-table.md). Il valore di componentkey rimane vuoto e non viene sostituito da una directory finché il programma di installazione non esegue l'azione \[ $  \] [CostInitialize](costinitialize-action.md), [l'azione FileCost](filecost-action.md)e [l'azione CostFinalize](costfinalize-action.md). Il valore di \[ $ *componentkey* \] dipende dallo stato di installazione del componente. Se il componente viene eseguito dall'origine, il valore è la directory di origine del file. Se il componente viene eseguito in locale, il valore è la directory di destinazione dopo l'installazione. Se il componente è assente, il valore viene lasciato vuoto. Per altre informazioni sul controllo dello stato di installazione dei componenti, vedere [Controllo dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
    -   Se viene trovata una sottostringa nel formato " c ", viene sostituita dal \[ \\ carattere senza ulteriori \] elaborazioni. Viene mantenuto solo il primo carattere dopo la barra rovesciata. tutti gli altri elementi vengono rimossi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Formattato](formatted.md)
</dt> <dt>

[Tipi di dati delle colonne](column-data-types.md)
</dt> </dl>

 

 




