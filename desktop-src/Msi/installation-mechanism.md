---
description: "Il processo di installazione ha esito positivo in due fasi: acquisizione ed esecuzione. Se l'installazione non riesce, può verificarsi una fase di rollback."
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Meccanismo di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bce4396701ab5cddb43a67dddbafd1e8310092d04d779af04ad7876681cc3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634219"
---
# <a name="installation-mechanism"></a>Meccanismo di installazione

Il processo di installazione ha esito positivo in due fasi: acquisizione ed esecuzione. Se l'installazione non riesce, può verificarsi una fase di rollback.

## <a name="acquisition"></a>Acquisizione

All'inizio della fase di acquisizione, un'applicazione o un utente indica al programma di installazione di installare una funzionalità o un'applicazione. Il programma di installazione procede quindi con le azioni specificate nelle tabelle di sequenza del database di installazione. Queste azioni eseguono query sul database di installazione e generano uno script che fornisce una procedura dettagliata per l'esecuzione dell'installazione.

## <a name="execution"></a>Esecuzione

Durante la fase di esecuzione, il programma di installazione passa le informazioni a un processo con privilegi elevati ed esegue lo script.

## <a name="rollback"></a>Rollback

Se un'installazione non riesce, il programma di installazione ripristina lo stato originale del computer. Quando il programma di installazione elabora lo script di installazione, genera contemporaneamente uno script di rollback. Oltre allo script di rollback, il programma di installazione salva una copia di ogni file eliminato durante l'installazione. Questi file vengono mantenuti in una directory di sistema nascosta. Al termine dell'installazione, lo script di rollback e i file salvati vengono eliminati. Per altre informazioni, vedere [Rollback installation](rollback-installation.md).

 

 



