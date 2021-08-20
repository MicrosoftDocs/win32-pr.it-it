---
description: Un esempio di uso di query di database guidate da script è disponibile in Windows Installer Software Development Kit (SDK) come utilità WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Esempi di query di database che usano SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137927ba47c4fae5eef4534b7dfab1fa5c8fa1af2ba28d27669cc4605f836b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947088"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Esempi di query di database che usano SQL e script

Un esempio di utilizzo di query di database guidate da script è disponibile in Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) come utilità WiRunSQL.vbs. Questa utilità gestisce le query di database usando la Windows installer di SQL descritta nella sezione SQL [Sintassi](sql-syntax.md).

**Eliminare un record da una tabella**

La riga di comando seguente elimina il record con la chiave primaria RED dalla [tabella Feature](feature-table.md) Test.msi database.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` Feature WHERE Feature \` \` \` . \` Funzionalità \` ='RED'"**

**Aggiungere una tabella a un database**

La riga di comando seguente aggiunge la [tabella Directory](directory-table.md) al database Test.msi database.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory ( \` Directory \` \` CHAR(72) NOT NULL, \` Directory Parent \_ \` CHAR(72), \` DefaultDir \` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \` Directory \` )"**

**Rimuovere una tabella da un database**

La riga di comando seguente rimuove la [tabella Feature](feature-table.md) dal database Test.msi database.

**Cscript WiRunSQL.vbs Test.msi "Funzionalità DROP \` \` TABLE"**

**Aggiungere una nuova colonna a una tabella**

La riga di comando seguente aggiunge la colonna Test alla [tabella CustomAction](customaction-table.md) del database Test.msi database.

**Codice CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` ADD Test \` \` INTEGER"**

**Inserire un nuovo record in una tabella**

La riga di comando seguente inserisce un nuovo record nella [tabella Feature](feature-table.md) del database Test.msi database.

**Cscript WiRunSQL.vbs Test.msi "Insert INTO \` Feature ( Feature \` \` \` . \` Funzionalità \` , \` Funzionalità \` . \` Elemento \_ padre \` della funzionalità, Funzionalità \` \` . \` Titolo, \` \` Funzionalità \` . \` Descrizione \` , \` Funzionalità \` . \` Visualizzare \` , \` Funzionalità \` . \` Livello \` , \` Funzionalità \` . \` Directory \_ \` , Funzionalità \` \` . \` Attributi \` ) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**

Il record seguente viene inserito nella [tabella Feature](feature-table.md) di Test.msi.

[Funzionalità](feature-table.md) tavolo



| Funzionalità | Elemento \_ padre della funzionalità | Titolo  | Descrizione | Visualizza | Level | Directory\_ | Attributi |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tennis  | Sport           | Tennis | Torneo  | 25      | 3     | SPORTDIR    | 2          |



 

Si noti che i dati binari non possono essere inseriti direttamente in una tabella usando le query INSERT INTO o UPDATE SQL query. Per informazioni, vedere [Aggiunta di dati binari a una tabella usando SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificare un record esistente in una tabella**

La riga di comando seguente modifica il valore esistente nel campo Titolo in "Prestazioni". Il record aggiornato ha "Arti" come chiave primaria e si trova nella tabella Funzionalità del database Test.msi database.

**Cscript WiRunSQL.vbs Test.msi "Update \` Feature SET Feature Feature \` \` \` . \` Title \` ='Performances' WHERE \` Feature \` . \` Feature \` ='Art'"**

**Selezionare un gruppo di record**

La riga di comando seguente seleziona il nome e il tipo di tutti i controlli che appartengono a ErrorDialog nel database Test.msi dati.

**CScript WiRunSQL.vbs Test.msi "SELECT \` Control \` , Type FROM Control WHERE Dialog \` \` \` \` \` \_ \` ='ErrorDialog' "**

**Mantenere una tabella in memoria**

La riga di comando seguente blocca la [tabella Component](component-table.md) del database Test.msi in memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` HOLD"**

**Liberare una tabella in memoria**

La riga di comando seguente libera la [tabella Component](component-table.md) del database Test.msi dalla memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` FREE"**

 

 



