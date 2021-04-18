---
description: Il metodo ApplyTransform dell'oggetto di database applica la trasformazione al database.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Metodo database. ApplyTransform
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
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331616"
---
# <a name="databaseapplytransform-method"></a>Metodo database. ApplyTransform

Il metodo **ApplyTransform** dell'oggetto di [**database**](database-object.md) applica la trasformazione al database.

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

Percorso del file di trasformazione da applicare. Questo parametro è obbligatorio.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Specifica le condizioni di errore che devono essere evitate. Specificare come una combinazione dei valori interi seguenti.



| Condizione di errore                                                                                                                                                                                                                                                                                                                                                  | Significato                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt></dt> <dt>0x0001</dt> msiTransformErrorAddExistingRow </dl>                                 | Aggiunge una riga già esistente.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt></dt> <dt>0x0002</dt> msiTransformErrorDeleteNonExistingRow </dl>         | Elimina una riga inesistente.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt></dt> <dt>0x0004</dt> msiTransformErrorAddExistingTable </dl>                         | Aggiunge una tabella già esistente.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt></dt> <dt>0x0008</dt> msiTransformErrorDeleteNonExistingTable </dl> | Elimina una tabella che non esiste.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt></dt> <dt>0x0010</dt> msiTransformErrorUpdateNonExistingRow </dl>         | Aggiorna una riga che non esiste.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt></dt> <dt>0x0020</dt> msiTransformErrorChangeCodePage </dl>                                 | Le tabelle codici di trasformazione e database non corrispondono e nessuna tabella codici è neutra.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt></dt> <dt>0x0100</dt> msiTransformErrorViewTransform </dl>                                     | Crea la [ \_ tabella transformview](-transformview-table.md)temporanea.<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **ApplyTransform** ritarda la trasformazione delle tabelle fino all'ultimo momento possibile. I passaggi eseguiti in **ApplyTransform** sono la trasformazione immediata dei cataloghi di tabelle e colonne per il database. I cataloghi della tabella e della colonna vengono aggiornati in base alla tabella aggiunta o eliminata e alla colonna aggiunta (non è consentita l'eliminazione di colonne). Se una tabella è attualmente caricata in memoria e deve essere trasformata, viene trasformata. In caso contrario, lo stato della tabella viene impostato su che richiede una trasformazione in modo che quando viene caricata la tabella o quando viene eseguito il commit del database, viene applicata la trasformazione. La trasformazione in questa istanza indica che i dati effettivi (riga) della tabella vengono aggiunti, eliminati o aggiornati.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> </dl>

 

 




