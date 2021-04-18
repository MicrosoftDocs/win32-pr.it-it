---
description: La Proprietà ColumnInfo dell'oggetto View restituisce un oggetto record contenente le informazioni richieste su ogni colonna del set di risultati.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Proprietà View. ColumnInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327173"
---
# <a name="viewcolumninfo-property"></a>Proprietà View. ColumnInfo

La proprietà **ColumnInfo** dell'oggetto [**View**](view-object.md) restituisce un oggetto [**record**](record-object.md) contenente le informazioni richieste su ogni colonna del set di risultati. È possibile che vengano richiesti i nomi di colonna o le definizioni delle colonne. Le costanti fornite nell'elenco di selezione non hanno nomi.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valore proprietà

Informazioni necessarie per ogni colonna.



| Nome parametro                                                                                                                                                                                                                                                          | Significato                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Restituisce i nomi di tutte le colonne non costanti nel set di risultati.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Restituisce i tipi di tutte le colonne non costanti nel set di risultati.<br/> |



 

## <a name="remarks"></a>Commenti

Le descrizioni delle colonne restituite dalla proprietà **ColumnInfo** sono nel formato descritto in [formato di definizione di colonna](column-definition-format.md). Ogni colonna è descritta da una stringa nel campo record corrispondente. La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri quando applicabile o da altri byte). Uno spessore pari a zero indica una larghezza senza limiti (campi di testo lunghi e flussi). Una lettera maiuscola indica che nella colonna sono consentiti valori null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




