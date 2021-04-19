---
description: "Ci sono due fasi per un processo di installazione completato: acquisizione ed esecuzione. Se l'installazione ha esito negativo, è possibile che si verifichi una fase di rollback."
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Meccanismo di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308902"
---
# <a name="installation-mechanism"></a>Meccanismo di installazione

Ci sono due fasi per un processo di installazione completato: acquisizione ed esecuzione. Se l'installazione ha esito negativo, è possibile che si verifichi una fase di rollback.

## <a name="acquisition"></a>Acquisizione

All'inizio della fase di acquisizione, un'applicazione o un utente indica al programma di installazione di installare una funzionalità o un'applicazione. Il programma di installazione procede quindi attraverso le azioni specificate nelle tabelle di sequenza del database di installazione. Queste azioni eseguono una query sul database di installazione e generano uno script che fornisce una procedura dettagliata per l'esecuzione dell'installazione.

## <a name="execution"></a>Esecuzione

Durante la fase di esecuzione, il programma di installazione passa le informazioni a un processo con privilegi elevati ed esegue lo script.

## <a name="rollback"></a>Rollback

Se un'installazione ha esito negativo, il programma di installazione ripristina lo stato originale del computer. Quando il programma di installazione elabora lo script di installazione, genera contemporaneamente uno script di rollback. Oltre allo script di rollback, il programma di installazione salva una copia di tutti i file eliminati durante l'installazione. Questi file vengono conservati in una directory di sistema nascosta. Al termine dell'installazione, vengono eliminati lo script di rollback e i file salvati. Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).

 

 



