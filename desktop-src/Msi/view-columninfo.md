---
description: La proprietà ColumnInfo dell'oggetto View restituisce un oggetto Record contenente le informazioni richieste su ogni colonna nel set di risultati.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View.ColumnInfo - proprietà
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
ms.openlocfilehash: 08996c3e77212032eac8f65621c7f8ca9ee8489683295c63fb30092995ad41d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012702"
---
# <a name="viewcolumninfo-property"></a>View.ColumnInfo - proprietà

La **proprietà ColumnInfo** dell'oggetto [**View**](view-object.md) restituisce un [**oggetto Record**](record-object.md) contenente le informazioni richieste su ogni colonna nel set di risultati. È possibile richiedere i nomi di colonna o le definizioni di colonna. Le costanti fornite nell'elenco Seleziona non hanno nomi.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valore proprietà

Informazioni necessarie per ogni colonna.



| Nome parametro                                                                                                                                                                                                                                                          | Significato                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Restituisce i nomi di tutte le colonne non conformi nel set di risultati.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Restituisce i tipi di tutte le colonne non conformi nel set di risultati.<br/> |



 

## <a name="remarks"></a>Commenti

Le descrizioni delle colonne restituite dalla **proprietà ColumnInfo** hanno il formato descritto in [Formato definizione colonna](column-definition-format.md). Ogni colonna è descritta da una stringa nel campo record corrispondente. La stringa di definizione è costituita da una singola lettera che rappresenta il tipo di dati seguito dalla larghezza della colonna (in caratteri, se applicabile, oppure byte diversi). Una larghezza pari a zero definisce una larghezza non associata (flussi e campi di testo lunghi). Una lettera maiuscola indica che nella colonna sono consentiti valori Null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView è definito come \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




