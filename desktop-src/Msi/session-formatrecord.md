---
description: Il metodo FormatRecord dell'oggetto Session restituisce una stringa formattata da un modello e registra i dati.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. FormatRecord, metodo
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
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327791"
---
# <a name="sessionformatrecord-method"></a>Session. FormatRecord, metodo

Il metodo **FormatRecord** dell'oggetto [**Session**](session-object.md) restituisce una stringa formattata da un modello e registra i dati.

## <a name="syntax"></a>Sintassi


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*record* 
</dt> <dd>

Oggetto **record** obbligatorio contenente un modello e i dati da formattare. La stringa di modello deve essere impostata nel campo 0 seguito da qualsiasi parametro di dati a cui si fa riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **FormatRecord** usa il processo di formato seguente.

I parametri da [formattare](formatted.md) sono racchiusi tra parentesi quadre \[ .. \] . È possibile scorrere le parentesi quadre perché le sostituzioni vengono risolte dall'interno.

Se una parte della stringa è racchiusa tra parentesi graffe {} e non contiene parentesi quadre, la parte viene lasciata invariata, comprese le parentesi graffe.

Se una parte della stringa è racchiusa tra parentesi graffe e contiene uno o più nomi di proprietà e se vengono trovate tutte le proprietà, il testo (con le sostituzioni risolte) viene visualizzato senza le parentesi graffe. Se una qualsiasi delle proprietà non viene trovata, tutto il testo racchiuso tra parentesi graffe e parentesi graffe vengono rimosse.

**Per formattare le stringhe usando il metodo FormatRecord**

1.  I parametri numerici vengono sostituiti sostituendo il marcatore con il valore del campo record corrispondente, con valori mancanti o null che non producono testo.
2.  La stringa risultante viene elaborata sostituendo i parametri non record con i valori corrispondenti, come indicato nelle descrizioni seguenti.
    -   Se viene rilevata una sottostringa nel formato " \[ PropertyName \] ", questa viene sostituita dal valore della proprietà.
    -   Se viene trovata una sottostringa nel formato " \[ % Metodo EnvironmentVariable \] ", il valore della variabile di ambiente viene sostituito.
    -   Se viene trovata una sottostringa del modulo \[ \# *FileKey* \] , questa viene sostituita dal percorso completo del file, con il valore *FileKey* usato come chiave nella [tabella file](file-table.md). Il valore di \[ \# *FileKey* \] rimane vuoto e non viene sostituito da un percorso fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md). Il valore di \[ \# *FileKey* \] dipende dallo stato di installazione del componente a cui appartiene il file. Se il componente viene eseguito dall'origine, il valore è il percorso della posizione di origine del file. Se il componente viene eseguito localmente, il valore è il percorso della posizione di destinazione del file dopo l'installazione. Se il componente è assente, il percorso è vuoto. Per ulteriori informazioni sul controllo dello stato di installazione dei componenti di, vedere [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
    -   Se viene trovata una sottostringa del modulo \[ *$componentkey* \] , questa viene sostituita dalla directory di installazione del componente, con il valore *componentkey* usato come chiave nella tabella dei [componenti](component-table.md). Il valore di \[ $ *componentkey* \] rimane vuoto e non viene sostituito da una directory fino a quando il programma di installazione non esegue l'azione [CostInitialize](costinitialize-action.md), l' [azione filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md). Il valore di \[ $ *componentkey* \] dipende dallo stato di installazione del componente. Se il componente viene eseguito dall'origine, il valore è la directory di origine del file. Se il componente viene eseguito localmente, il valore è la directory di destinazione dopo l'installazione. Se il componente è assente, il valore viene lasciato vuoto. Per ulteriori informazioni sul controllo dello stato di installazione dei componenti di, vedere [Verifica dell'installazione di funzionalità, componenti, file](checking-the-installation-of-features-components-files.md).
    -   Se viene trovata una sottostringa nel formato " \[ \\ c \] ", questa viene sostituita dal carattere senza ulteriori elaborazioni. Viene mantenuto solo il primo carattere dopo la barra rovesciata; tutte le altre operazioni vengono rimosse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Formattato](formatted.md)
</dt> <dt>

[Tipi di dati delle colonne](column-data-types.md)
</dt> </dl>

 

 




