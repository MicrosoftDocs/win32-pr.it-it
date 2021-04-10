---
description: ICE45 verifica che le colonne del campo di bit nel database non impostino bit riservati su 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227197"
---
# <a name="ice45"></a>ICE45

ICE45 verifica che le colonne del campo di bit nel database non impostino bit riservati su 1.

I bit riservati non forniscono funzionalità nelle versioni correnti del programma di installazione, ma potrebbero nelle versioni future. Devono essere impostati su 0 per essere compatibili con le versioni future di Windows Installer.

## <a name="result"></a>Risultato

ICE45 Invia un messaggio di errore se una delle tabelle seguenti contiene un campo di bit con un bit riservato impostato su un valore pari a 1.

-   [Tabella BBControl](bbcontrol-table.md)
-   [Tabella finestra di dialogo](dialog-table.md)
-   [Tabella delle funzionalità](feature-table.md)
-   [Tabella file](file-table.md)
-   [Tabella MoveFile](movefile-table.md)
-   [Tabella ModuleConfiguration](moduleconfiguration-table.md)
-   [Tabella ODBCDataSource](odbcdatasource-table.md)
-   [Tabella patch](patch-table.md)
-   [Tabella RemoveFile](removefile-table.md)
-   [Tabella ServiceControl](servicecontrol-table.md)
-   [Tabella ServiceInstall](serviceinstall-table.md)
-   [Tabella TextStyle](textstyle-table.md)

ICE45 invia uno dei due messaggi di avviso se la [tabella di controllo](control-table.md) contiene un campo di bit con un bit riservato impostato su un valore pari a 1.

## <a name="example"></a>Esempio

ICE45 segnala l'errore seguente per l'esempio illustrato.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Tabella file](file-table.md) (parziale)



| File  | Attributi |
|-------|------------|
| File1 | 128        |



 

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control | Attributi |
|---------|---------|------------|
| Dialog1 | Edit1   | 2097152    |
| Dialog1 | Edit2   | 1048576    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



