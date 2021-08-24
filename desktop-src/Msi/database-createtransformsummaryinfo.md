---
description: Il metodo CreateTransformSummaryInfo dell'oggetto Database crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente. Questo metodo inserisce nelle proprietà la base e fa riferimento a ProductCode e ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Metodo Database.CreateTransformSummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e1daa3e31ccfb49e49842994d6203b58534d86c111cd98652e66079fa47322cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745731"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Metodo Database.CreateTransformSummaryInfo

Il **metodo CreateTransformSummaryInfo** dell'oggetto [**Database**](database-object.md) crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente. Questo metodo inserisce le proprietà con la base e fa riferimento [**a ProductCode**](productcode.md) e [**ProductVersion.**](productversion.md)

## <a name="syntax"></a>Sintassi


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*reference* 
</dt> <dd>

Database obbligatorio che non include le modifiche.

</dd> <dt>

*storage* 
</dt> <dd>

Nome del file di trasformazione generato. Questo indirizzo è facoltativo.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Condizioni di errore obbligatorie che devono essere soppresse quando viene applicata la trasformazione. Combinare uno o più dei valori di condizione di errore seguenti.



| Nome condizione di errore                                                                                                                                                                                                                                                                                                                                        | Significato                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msiTransformErrorNone**</dt> <dt>0</dt> </dl>                                                                         | Nessuna delle condizioni seguenti.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt> </dl>                                 | Aggiunge una riga già esistente.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt> </dl>         | Elimina una riga che non esiste.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt> </dl>                         | Aggiunge una tabella già esistente.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt> </dl> | Elimina una tabella che non esiste.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt> </dl>        | Aggiorna una riga che non esiste.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt> </dl>                                | Le tabelle codici di trasformazione e di database non corrispondono e nessuna delle due tabelle codici è neutra.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Obbligatorio quando la trasformazione viene applicata a un database. mostra le proprietà da convalidare per verificare che questa trasformazione possa essere applicata al database. Tutte le proprietà sono contenute nel [set di proprietà Summary Information Stream](summary-information-stream-property-set.md).

Combinare uno o più dei valori seguenti.



| Flag di convalida                                                                                                                                                                                                                                                                                                         | Significato                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msiTransformValidationNone**</dt> <dt>0</dt> </dl>                 | Nessuna convalida eseguita.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msiTransformValidationLanguage**</dt> <dt>1</dt> </dl> | La lingua predefinita deve corrispondere al database di base.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msiTransformValidationProduct**</dt> <dt>2</dt> </dl>     | Il prodotto deve corrispondere al database di base.<br/>          |



 

Per convalidare la versione del prodotto, scegliere prima uno o più di questi tre flag per indicare la quantità di versione da verificare.



| Flag di convalida                                                                                                                                                                                                                                                                                                              | Significato                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt> </dl>      | Controlla solo la versione principale.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt> </dl>     | Controlla solo la versione principale e secondaria.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt> </dl> | Controlla le versioni principali, secondarie e di aggiornamento.<br/> |



 

Scegliere quindi una delle opzioni seguenti per indicare la relazione necessaria tra la versione del prodotto del database a cui viene applicata la trasformazione e quella del database di base.



| Flag di convalida                                                                                                                                                                                                                                                                                                                                   | Significato                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msiTransformValidationLess**</dt> <dt>64</dt> </dl>                                          | Versione applicata < base<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt> </dl>             | Versione applicata <= versione di base<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msiTransformValidationEqual**</dt> <dt>256</dt> </dl>                                     | Versione applicata = versione di base<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt> </dl> | Versione applicata >= versione di base<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msiTransformValidationGreater**</dt> <dt>1024</dt> </dl>                            | Versione applicata > base<br/>  |



 

Per verificare che la trasformazione venga applicata a un pacchetto con [**il codice di aggiornamento appropriato,**](upgradecode.md)impostare il flag seguente.



| Flag di convalida                                                                                                                                                                                                                                                                                                                        | Significato                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt> </dl> | Verifica che la trasformazione sia l'oggetto [**UpgradeCode appropriato.**](upgradecode.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per creare un flusso di informazioni di riepilogo per una trasformazione, le proprietà [**ProductCode**](productcode.md) e [**ProductVersion**](productversion.md) devono essere definite nelle tabelle [delle](property-table.md) proprietà dei database di base e di riferimento. Se si usa msiTransformValidationUpgradeCode, la [**proprietà UpgradeCode**](upgradecode.md) deve essere definita in entrambi i database.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> </dl>

 

 




