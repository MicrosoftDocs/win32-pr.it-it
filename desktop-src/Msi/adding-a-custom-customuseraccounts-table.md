---
description: Una specifica dell'esempio è che le informazioni sull'account utente vengono lette da una tabella personalizzata nel database di installazione e non hard coded nell'azione personalizzata.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Aggiunta di una tabella CustomUserAccounts personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede08ad733e2870e970416da3de345bfc89b7e63147bc848f3d36ffe66721585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066461"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Aggiunta di una tabella CustomUserAccounts personalizzata

Una specifica dell'esempio è che le informazioni sull'account utente vengono lette da una tabella personalizzata nel database di installazione e non hard coded nell'azione personalizzata.

Aggiungere una tabella personalizzata al database di installazione di esempio denominato CustomUserAccounts per contenere le informazioni sull'account utente. Per un esempio su come aggiungere una tabella [personalizzata, vedere Esempi](examples-of-database-queries-using-sql-and-script.md) di query di database SQL e script. Usare lo schema seguente per la tabella CustomUserAccounts. Per [una spiegazione dei tipi di](column-definition-format.md) colonna, vedere Formato definizione colonna.



| Colonna     | Tipo | Chiave | Nullable | Descrizione                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | S   | N        | Nome dell'account utente da creare.                                                                                                                                                                                                                                                                        |
| Password   | s72  |     | N        | Nome della proprietà contenente la password per l'account. Si tratta di [una proprietà pubblica](public-properties.md) impostata nella riga di comando o tramite un controllo di [modifica](edit-control.md) nell'interfaccia utente. Questo controllo di modifica deve avere [l'attributo di controllo password](password-control-attribute.md). |
| Attributi | i4   |     | S        | Attributi per l'account. Questi valori sono definiti come **valori DWORD** per il membro flag usri1 \_ della struttura USER INFO \_ \_ 1.                                                                                                                                                                              |



 

Dopo aver aggiunto la tabella CustomUserAccounts al database, è possibile modificarla usando Orca, un editor di tabelle fornito con Windows Installer SDK o un altro editor. Immettere il record seguente nella tabella CustomUserAccounts per creare un account utente protetto da password per un utente di nome TestUser. Si noti che 512 è il valore numerico per UF \_ NORMAL \_ ACCOUNT.

Tabella CustomUserAccounts



| UserName | Password         | Attributi |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

Aggiungere i record seguenti alla \_ tabella Validation per la tabella personalizzata.

[\_Tabella di convalida](-validation-table.md)



| Tabella              | Colonna     | Nullable | Minvalue | MaxValue   | KeyTable | KeyColumn | Category                     | Impostazione | Descrizione |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | Nome utente   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Password   | N        |          |            |          |           | [Identificatore](identifier.md) |     |             |
| CustomUserAccounts | Attributi | S        | 0        | 2147483647 |          |           | Null                         |     |             |



 

Continuare a [creare le tabelle ActionText ed Error](authoring-the-actiontext-and-error-tables.md).

 

 



