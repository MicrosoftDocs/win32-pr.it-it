---
description: Il metodo ApplyTransform dell'oggetto Database applica la trasformazione al database.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Metodo Database.ApplyTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9c3424dab82b6981af033b40b33481937fd7c36d3c00dcf3ddfcba5f13f56ec7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289621"
---
# <a name="databaseapplytransform-method"></a>Metodo Database.ApplyTransform

Il **metodo ApplyTransform** dell'oggetto [**Database**](database-object.md) applica la trasformazione al database.

## <a name="syntax"></a>Sintassi


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*storage* 
</dt> <dd>

Percorso del file di trasformazione applicato. Questo parametro è obbligatorio.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Specifica le condizioni di errore da eliminare. Specificare come combinazione dei valori integer seguenti.



| Condizione di errore                                                                                                                                                                                                                                                                                                                                                  | Significato                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**MsiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | Aggiunge una riga già esistente.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**MsiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | Elimina una riga che non esiste.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**MsiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | Aggiunge una tabella già esistente.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**MsiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | Elimina una tabella che non esiste.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**MsiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | Aggiorna una riga che non esiste.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**MsiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | Le tabelle codici di trasformazione e di database non corrispondono e nessuna delle due ha una tabella codici neutra.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**MsiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Crea la tabella [ \_ TransformView temporanea.](-transformview-table.md)<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo ApplyTransform** ritarda la trasformazione delle tabelle fino all'ultimo momento possibile. La procedura eseguita in **ApplyTransform** è di trasformare immediatamente i cataloghi di tabelle e colonne per il database. I cataloghi di tabelle e colonne vengono aggiornati in base alla tabella aggiunta o eliminata e alla colonna aggiunta (non è consentita alcuna eliminazione di colonne). Se una tabella è attualmente caricata in memoria e deve essere trasformata, viene trasformata. In caso contrario, lo stato della tabella viene impostato su che richiede una trasformazione in modo che quando la tabella viene caricata o quando viene eseguito il commit del database, la trasformazione viene applicata. Trasforma in questa istanza significa che i dati effettivi (riga) della tabella vengono aggiunti, eliminati o aggiornati.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[Trasformazioni del database](database-transforms.md)
</dt> </dl>

 

 




