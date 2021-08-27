---
description: Il metodo GenerateTransform dell'oggetto Database crea una trasformazione che, se applicata al database di oggetti, restituisce il database di riferimento. La trasformazione viene archiviata nell'oggetto di archiviazione.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Metodo Database.GenerateTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c07e7483a43ea4f69eac473c76747447932fba57e53e22f79fa0663d4babc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129651"
---
# <a name="databasegeneratetransform-method"></a>Metodo Database.GenerateTransform

Il **metodo GenerateTransform** dell'oggetto [**Database**](database-object.md) crea una [*trasformazione*](t-gly.md) che, se applicata al database di oggetti, restituisce il database di riferimento. La trasformazione viene archiviata nell'oggetto di archiviazione.

Se la trasformazione deve essere applicata durante un'installazione, è necessario usare il [**metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) per popolare il flusso di informazioni di riepilogo.

## <a name="syntax"></a>Sintassi


```JScript
Database.GenerateTransform(
  reference,
  storage
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Una trasformazione può aggiungere colonne chiave non primaria alla fine di una tabella. Non è possibile creare una trasformazione che aggiunge colonne chiave primaria a una tabella. Non è possibile creare una trasformazione che modifica l'ordine, i nomi o le definizioni delle colonne.

Questo metodo restituisce un valore booleano. Restituisce TRUE se viene generata una trasformazione. Restituisce FALSE se non viene generata una trasformazione perché non esistono differenze tra i due database. Se il metodo ha esito negativo, viene generato un errore.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Database**](database-object.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> </dl>

 

 




