---
description: Il metodo GenerateTransform dell'oggetto di database crea una trasformazione che, quando applicata al database dell'oggetto, restituisce il database di riferimento. La trasformazione viene archiviata nell'oggetto di archiviazione.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Metodo database. GenerateTransform
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
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326899"
---
# <a name="databasegeneratetransform-method"></a>Metodo database. GenerateTransform

Il metodo **GenerateTransform** dell'oggetto di [**database**](database-object.md) crea una [*trasformazione*](t-gly.md) che, quando applicata al database dell'oggetto, restituisce il database di riferimento. La trasformazione viene archiviata nell'oggetto di archiviazione.

Se la trasformazione deve essere applicata durante un'installazione, è necessario usare il metodo [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) per popolare il flusso di informazioni di riepilogo.

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

Una trasformazione può aggiungere colonne chiave non primarie alla fine di una tabella. Non è possibile creare una trasformazione che aggiunge colonne chiave primaria a una tabella. Non è possibile creare una trasformazione che modifichi l'ordine, i nomi o le definizioni delle colonne.

Questo metodo restituisce un valore booleano. Restituisce TRUE se viene generata una trasformazione. Restituisce FALSE se non viene generata alcuna trasformazione perché non vi sono differenze tra i due database. Se il metodo ha esito negativo, viene generato un errore.

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

 

 




