---
description: Il metodo Merge dell'oggetto di database unisce il database di riferimento al database di base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Metodo database. merge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Merge
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0a1d93ba6a9a4dc0304daba11c5868b77ece43b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329752"
---
# <a name="databasemerge-method"></a>Metodo database. merge

Il metodo **merge** dell'oggetto di [**database**](database-object.md) unisce il database di riferimento al database di base.

## <a name="syntax"></a>Sintassi


```JScript
Database.Merge(
  reference,
  errorTable
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*reference* 
</dt> <dd>

Oggetto di [**database**](database-object.md) obbligatorio da unire nel database.

</dd> <dt>

*errorTable* 
</dt> <dd>

Nome facoltativo di una tabella che contiene i nomi delle tabelle contenenti conflitti di merge, il numero di righe in conflitto all'interno della tabella e un riferimento alla tabella con il conflitto di Unione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Non è possibile usare la funzione [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e il metodo **merge** dell'oggetto di [**database**](database-object.md) per unire un modulo incluso in un pacchetto di installazione. Non devono essere utilizzate per unire i [moduli unione](merge-modules.md) in un pacchetto di Windows Installer. Per includere un modulo merge in un pacchetto di installazione, è necessario che gli autori dei pacchetti di installazione seguano le linee guida descritte nell'argomento [Applying merge modules](applying-merge-modules.md) .

Il metodo **merge** non esegue la copia su [file CAB](cabinet-files.md) incorporati o [trasformazioni incorporate](embedded-transforms.md) dal database di riferimento nel database di destinazione. I flussi di dati incorporati elencati nella tabella [binaria](binary-table.md) o nella [tabella delle icone](icon-table.md) vengono copiati dal database di riferimento al database di destinazione. Le archiviazioni incorporate nel database di riferimento non vengono copiate nel database di destinazione.

Se non viene fornita alcuna tabella, il messaggio di errore generale fornisce il numero di tabelle contenenti conflitti di merge. È possibile passare qualsiasi tabella, ma tutte le altre colonne devono ammettere i valori null perché l'operazione di aggiornamento della [tabella degli errori](error-table.md) ha esito negativo se una colonna non ammette i valori null. È anche possibile passare una tabella appena creata, perché il metodo **merge** crea automaticamente le colonne che utilizza se vengono rilevati conflitti di merge. Per presentare conflitti di merge vengono utilizzate due colonne. La prima colonna è il nome della tabella e la colonna chiave primaria. La seconda colonna indica il numero di righe della tabella in cui sono presenti errori di Unione.

Se le tabelle con lo stesso nome in entrambi i database non corrispondono al numero di chiavi primarie, ai tipi di colonna, al numero di colonne o ai nomi delle colonne, il metodo **merge** ha esito negativo e invia un messaggio di errore che indica che cosa si è verificato.

Affinché la tabella degli errori rimanga, il gestore degli errori deve eseguire il commit del database a cui appartiene la tabella degli errori. Tuttavia, questo commit deve essere eseguito dopo l'utilizzo della terza colonna per ottenere i riferimenti alle tabelle in cui si sono verificati i conflitti di Unione.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




