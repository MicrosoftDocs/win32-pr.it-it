---
description: '\\Client HKLM Software \\ Microsoft \\ MSSQLSERVER \\ .'
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049161"
---
# <a name="connectto"></a>ConnectTo

**\\Client HKLM Software \\ Microsoft \\ MSSQLSERVER \\**

## <a name="description"></a>Descrizione

La sottochiave **ConnectTo** archivia le informazioni di connessione per i client basati su Windows che si connettono alle istanze del motore di database Microsoft SQL Server. Le voci del registro di sistema in questa sottochiave sono di tipo di dati REG \_ SZ e i relativi valori specificano il Net-Library da usare per la connessione all'istanza di, nonché qualsiasi parametro specifico della rete.

Le informazioni di connessione archiviate in questa sottochiave vengono lette dal provider OLE DB per SQL Server, dal driver ODBC SQL Server o dal SQL Server DB-Library libreria a collegamento dinamico (DLL).

## <a name="change-method"></a>Cambia metodo

Non è necessario modificare le voci in questa sottochiave utilizzando l'editor del registro di sistema. Utilizzare l'utilità di rete client di SQL Server per configurare il nome del server e le informazioni di connessione. Per altre istruzioni, vedere SQL Server Guida dell'utilità di rete client.

## <a name="notes"></a>Note

-   La sottochiave **ConnectTo** viene utilizzata dal provider OLE DB per SQL Server, dal Driver ODBC SQL Server e dalla DLL di DB-Library SQL Server. Le voci della sottochiave identificano i Net-Library questi componenti API (Data Access Application Programming Interface) chiamano.
-   Net-Libraries sono componenti SQL Server che proteggono i componenti dell'API di accesso ai dati dai dettagli dell'utilizzo di metodi di comunicazione interprocesso (IPC) diversi per comunicare con un'istanza del motore di database SQL Server.
-   L'aggiornamento errato della sottochiave **ConnectTo** potrebbe impedire la corretta connessione delle applicazioni a un'istanza del motore di database SQL Server.

 

 



