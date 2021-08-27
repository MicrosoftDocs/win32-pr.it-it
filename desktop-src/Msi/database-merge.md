---
description: Il metodo Merge dell'oggetto Database unisce il database di riferimento al database di base.
ms.assetid: 777060cf-c672-49d5-a1a8-8674fdc4bde4
title: Metodo Database.Merge
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
ms.openlocfilehash: 4fad74e1647413b66ebc6910e739750699f4e641c961eff59ecaacbf1e7a41f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074991"
---
# <a name="databasemerge-method"></a>Metodo Database.Merge

Il **metodo Merge** dell'oggetto [**Database**](database-object.md) unisce il database di riferimento al database di base.

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

Oggetto [**Database**](database-object.md) necessario da unire nel database.

</dd> <dt>

*tabella errorTable* 
</dt> <dd>

Nome facoltativo di una tabella contenente i nomi delle tabelle contenenti conflitti di merge, il numero di righe in conflitto all'interno della tabella e un riferimento alla tabella con il conflitto di merge.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La [**funzione MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) e il **metodo Merge** dell'oggetto [**Database**](database-object.md) non possono essere usati per unire un modulo incluso in un pacchetto di installazione. Non devono essere usati per unire i [moduli unione](merge-modules.md) in un pacchetto Windows Installer. Per includere un modulo unione in un pacchetto di installazione, gli autori dei pacchetti di installazione devono seguire le linee guida descritte nell'argomento [Applicazione di moduli unione.](applying-merge-modules.md)

Il **metodo Merge** non copia i file [CAB](cabinet-files.md) incorporati o le [trasformazioni](embedded-transforms.md) incorporate dal database di riferimento nel database di destinazione. I flussi di dati incorporati elencati nella [tabella](binary-table.md) binaria o nella [tabella](icon-table.md) icona vengono copiati dal database di riferimento al database di destinazione. Le risorse di archiviazione incorporate nel database di riferimento non vengono copiate nel database di destinazione.

Se non viene specificata alcuna tabella, il messaggio di errore generale indica il numero di tabelle contenenti conflitti di merge. È possibile passare qualsiasi tabella, ma tutte le altre colonne [](error-table.md) devono essere nullable perché l'operazione di aggiornamento della tabella degli errori ha esito negativo se una colonna non ammette valori Null. È possibile passare anche una tabella appena creata perché il metodo **Merge** crea automaticamente le colonne utilizzate se vengono rilevati conflitti di merge. Per presentare conflitti di merge vengono utilizzate due colonne. La prima colonna è il nome della tabella e la colonna chiave primaria. La seconda colonna è il numero di righe della tabella con errori di merge.

Se le tabelle con lo stesso nome in entrambi i database non corrispondono nel numero di chiavi primarie, nei tipi di colonna, nel numero di colonne o nei nomi delle colonne, il metodo **Merge** ha esito negativo e viene inviato un messaggio di errore che indica che cosa si è verificato.

Per mantenere la tabella Error, il gestore degli errori deve eseguire il commit del database a cui appartiene la tabella Error. Tuttavia, questo commit deve essere eseguito dopo aver utilizzato la terza colonna per ottenere i riferimenti alle tabelle in cui si sono verificati conflitti di merge.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




