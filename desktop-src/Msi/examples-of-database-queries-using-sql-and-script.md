---
description: Un esempio di utilizzo di query di database basate su script viene fornito in Windows Installer SDK (Software Development Kit) come WiRunSQL.vbs di utilità.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Esempi di query sul database con SQL e script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755626"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a>Esempi di query sul database con SQL e script

Un esempio di utilizzo di query di database basate su script è disponibile nel [Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) di Windows Installer come utilità WiRunSQL.vbs. Questa utilità gestisce le query di database usando la versione Windows Installer di SQL descritta nella sezione [sintassi SQL](sql-syntax.md).

**Eliminare un record da una tabella**

La riga di comando seguente consente di eliminare il record con la chiave primaria rossa dalla tabella delle [funzionalità](feature-table.md) del database di Test.msi.

**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \` feature \` Where \` feature \` . \` Feature \` = "rosso" "**

**Aggiungere una tabella a un database**

La riga di comando seguente aggiunge la tabella di [directory](directory-table.md) al database Test.msi.

**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` directory \` ( \` directory \` char (72) not null, \` directory \_ Parent \` char (72), \` DefaultDir \` char (255) not null localizzable Primary Key \` directory \` )"**

**Rimuovere una tabella da un database**

La riga di comando seguente consente di rimuovere la tabella delle [funzionalità](feature-table.md) dal database Test.msi.

**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \` feature \` "**

**Aggiungere una nuova colonna a una tabella**

La riga di comando seguente aggiunge la colonna di test alla tabella [CustomAction](customaction-table.md) del database di Test.msi.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` CustomAction \` Add \` test \` Integer"**

**Inserire un nuovo record in una tabella**

Nella riga di comando seguente viene inserito un nuovo record nella tabella delle [funzionalità](feature-table.md) del database di Test.msi.

**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \` feature \` ( \` feature \` . \` Funzionalità \` \` \` . \` Funzionalità \_ \` , elemento \` padre \` . \` Titolo \` , \` funzionalità \` . \` Descrizione \` , \` funzionalità \` . \` Display \` , \` feature \` . \` Livello \` , \` funzionalità \` . \` Directory \_ \` , \` funzionalità \` . \` Attributi \` ) valori (' tennis ',' sport ',' tennis ',' Tournament ', 25, 3,' SPORTDIR ', 2) "**

Il record seguente viene inserito nella tabella delle [funzionalità](feature-table.md) di Test.msi.

[Funzionalità](feature-table.md) di tavolo



| Funzionalità | \_Elemento padre della funzionalità | Titolo  | Descrizione | Visualizza | Level | Directory\_ | Attributi |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| Tennis  | Sport           | Tennis | Tournament  | 25      | 3     | SPORTDIR    | 2          |



 

Si noti che non è possibile inserire dati binari in una tabella usando direttamente le query INSERT INTO o UPDATE SQL. Per informazioni, vedere [aggiunta di dati binari a una tabella con SQL](adding-binary-data-to-a-table-using-sql.md).

**Modificare un record esistente in una tabella**

La riga di comando seguente modifica il valore esistente nel campo title in "performances". Il record aggiornato contiene "Arts" come chiave primaria ed è presente nella tabella delle funzionalità del database di Test.msi.

**Cscript WiRunSQL.vbs Test.msi "aggiornare \` la \` funzionalità del set di funzionalità \` \` . \` Title \` = "performances" Where \` feature \` . \` Feature \` = "Arts" "**

**Seleziona un gruppo di record**

La riga di comando seguente consente di selezionare il nome e il tipo di tutti i controlli che appartengono a ErrorDialog nel database di Test.msi.

**CScript WiRunSQL.vbs Test.msi "selezionare il \` controllo \` , \` digitare \` da \` Control \` Where \` Dialog \_ \` =' ErrorDialog '"**

**Mantenere una tabella in memoria**

La riga di comando seguente blocca la tabella dei [componenti](component-table.md) del database Test.msi in memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` holding"**

**Liberare una tabella in memoria**

La riga di comando seguente libera la tabella dei [componenti](component-table.md) del database Test.msi dalla memoria.

**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \` Component \` Free"**

 

 



