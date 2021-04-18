---
description: Una specifica dell'esempio è che le informazioni dell'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hardcoded nell'azione personalizzata.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Aggiunta di una tabella CustomUserAccounts personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311084"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Aggiunta di una tabella CustomUserAccounts personalizzata

Una specifica dell'esempio è che le informazioni dell'account utente vengono lette da una tabella personalizzata nel database di installazione e non sono hardcoded nell'azione personalizzata.

Aggiungere una tabella personalizzata al database di installazione di esempio denominato CustomUserAccounts per conservare le informazioni dell'account utente. Per un esempio di come aggiungere una tabella personalizzata, vedere [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md) . Utilizzare lo schema seguente per la tabella CustomUserAccounts. Per una spiegazione dei tipi di colonna, vedere [formato della definizione di colonna](column-definition-format.md) .



| Colonna     | Tipo | Chiave | Nullable | Descrizione                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | S72  | S   | N        | Nome dell'account utente in fase di creazione.                                                                                                                                                                                                                                                                        |
| Password   | S72  |     | N        | Nome della proprietà contenente la password per l'account. Si tratta di una [proprietà pubblica](public-properties.md) impostata nella riga di comando o tramite un [controllo di modifica](edit-control.md) nell'interfaccia utente. Questo controllo di modifica deve avere l' [attributo di controllo password](password-control-attribute.md). |
| Attributi | i4   |     | S        | Attributi per l'account. Questi vengono definiti come valori **DWORD** per il \_ membro dei flag usri1 della struttura di \_ informazioni utente \_ 1.                                                                                                                                                                              |



 

Dopo che la tabella CustomUserAccounts è stata aggiunta al database, è possibile modificare la tabella usando Orca, un editor di tabelle fornito con Windows Installer SDK o un altro editor. Immettere il record seguente nella tabella CustomUserAccounts per creare un account utente protetto da password per un utente denominato TestUser. Si noti che 512 è il valore numerico per \_ l' \_ account UF Normal.

Tabella CustomUserAccounts



| UserName | Password         | Attributi |
|----------|------------------|------------|
| TestUser | TESTUSERPASSWORD | 512        |



 

Aggiungere i record seguenti alla \_ tabella di convalida per la tabella personalizzata.

[\_Tabella di convalida](-validation-table.md)



| Tabella              | Colonna     | Nullable | MinValue | MaxValue   | KeyTable | KeyColumn | Category                     | Set | Descrizione |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Password   | N        |          |            |          |           | [Identificatore](identifier.md) |     |             |
| CustomUserAccounts | Attributi | S        | 0        | 2147483647 |          |           | Null                         |     |             |



 

Continuare a [creare le tabelle ActionText e Error](authoring-the-actiontext-and-error-tables.md).

 

 



