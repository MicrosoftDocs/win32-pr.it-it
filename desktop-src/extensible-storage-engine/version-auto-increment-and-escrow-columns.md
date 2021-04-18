---
description: Altre informazioni sulle colonne versione, incremento automatico e deposito vincolato
title: Colonne versione, incremento automatico e escrow
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307789"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Colonne versione, incremento automatico e escrow


_**Si applica a:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Colonne versione, incremento automatico e escrow

ESE fornisce la versione, l'incremento automatico e i tipi di colonna di aggiornamento del deposito a garanzia con funzionalità speciali. Le opzioni di colonna impostate nel membro **grbit** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizzata nella chiamata a [JetAddColumn](./jetaddcolumn-function.md) indicano se la colonna è uno dei tipi specializzati indicati qui.

### <a name="version-jet_bitcolumnversion"></a>Versione (JET_bitColumnVersion)

L'opzione colonna versione, applicata solo a JET_coltypLong colonne, indica che la colonna contiene informazioni sulla versione del record che possono essere utilizzate per determinare se è necessario aggiornare una copia in memoria di un determinato record. Le colonne della versione vengono incrementate automaticamente da ESE quando la colonna viene modificata dall'applicazione tramite [JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automatico (JET_bitColumnAutoincrement)

Le colonne con incremento automatico vengono incrementate automaticamente da ESE quando viene inserito un nuovo record nella tabella. Il valore contenuto nella colonna incremento automatico è univoco per ogni record della tabella e non è garantito che sia continuo. Questi valori non vengono riciclati, ma possono essere riutilizzati in alcuni casi. Solo le colonne di tipo JET_coltypLong e JET_coltypLongLong possono essere colonne a incremento automatico.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Deposito vincolato (JET_bitColumnEscrowUpdate)

Le colonne escrow possono essere modificate nella chiamata a [JetEscrowUpdate](./jetescrowupdate-function.md). Gli aggiornamenti in escrow sono operazioni delta numeriche che non soffrono di conflitti di scrittura. Ciò significa che un numero qualsiasi di sessioni può aggiornare simultaneamente una colonna del deposito in un record tramite [JetEscrowUpdate](./jetescrowupdate-function.md) senza conflitti. Si noti che qualsiasi altra operazione di aggiornamento può comunque causare un conflitto di scrittura con un'operazione di aggiornamento del deposito. Gli aggiornamenti del deposito a garanzia possono essere apportati solo a colonne di tipo JET_coltypLong che hanno un valore predefinito. Queste colonne devono inoltre essere aggiunte a una tabella prima che vengano caricate con righe. Infine, le righe contenenti una colonna di aggiornamento del deposito possono essere configurate per supportare un callback di finalizzazione della riga (JET_bitColumnFinalize) o per essere eliminate automaticamente se il conteggio dei riferimenti raggiunge zero (JET_bitColumnDeleteOnZero). Per ulteriori informazioni, vedere la struttura [JET_COLUMNDEF](./jet-columndef-structure.md) .
