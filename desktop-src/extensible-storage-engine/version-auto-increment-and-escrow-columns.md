---
description: 'Altre informazioni su: Colonne Version, Auto-Increment e Escrow'
title: Colonne Version, Auto-Increment e Escrow
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: b86b37663f7968ad77874ebcc7b2d0f8fd569cc265424bc36feeecccb6d7e148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471281"
---
# <a name="version-auto-increment-and-escrow-columns"></a>Colonne Version, Auto-Increment e Escrow


_**Si applica a:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Colonne Version, Auto-Increment e Escrow

ESE fornisce i tipi di colonna versione, incremento automatico e aggiornamento deposito con funzionalità speciali. Le opzioni di colonna impostate nel membro **grbit** della struttura JET_COLUMNDEF usata nella chiamata [a](./jet-columndef-structure.md) [JetAddColumn](./jetaddcolumn-function.md) indicano se la colonna è uno dei tipi specializzati indicati qui.

### <a name="version-jet_bitcolumnversion"></a>Versione (JET_bitColumnVersion)

L'opzione version column, applicata solo JET_coltypLong colonne, indica che la colonna contiene informazioni sulla versione del record che possono essere usate per determinare se è necessario aggiornare una copia in memoria di un determinato record. Le colonne di versione vengono incrementate automaticamente da ESE quando la colonna viene modificata dall'applicazione tramite [JetUpdate](./jetupdate-function.md).

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automatico (JET_bitColumnAutoincrement)

Le colonne con incremento automatico vengono incrementate automaticamente da ESE quando viene inserito un nuovo record nella tabella. Il valore contenuto nella colonna con incremento automatico è univoco per ogni record nella tabella e non è garantito che sia continuo. Questi valori non vengono riciclati, ma possono essere riutilizzati in determinati casi. Solo le colonne di tipo JET_coltypLong e JET_coltypLongLong possono essere colonne con incremento automatico.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Deposito a garanzia (JET_bitColumnEscrowUpdate)

Le colonne di deposito possono essere modificate nella chiamata [a JetEscrowUpdate.](./jetescrowupdate-function.md) Gli aggiornamenti in deposito sono operazioni differenziali numeriche che non subiscono conflitti di scrittura. Ciò significa che qualsiasi numero di sessioni può aggiornare contemporaneamente una colonna di deposito in un record tramite [JetEscrowUpdate](./jetescrowupdate-function.md) senza conflitti. Si noti che qualsiasi altra operazione di aggiornamento può comunque causare un conflitto di scrittura con un'operazione di aggiornamento del deposito. Gli aggiornamenti del deposito possono essere emesse solo a colonne di JET_coltypLong con un valore predefinito. Queste colonne devono anche essere aggiunte a una tabella prima di essere caricate con righe. Infine, le righe contenenti una colonna di aggiornamento del deposito possono essere configurate per supportare un callback di finalizzazione delle righe (JET_bitColumnFinalize) o per essere eliminate automaticamente se il conteggio dei riferimenti raggiunge zero (JET_bitColumnDeleteOnZero). Per altre informazioni, vedere la struttura [JET_COLUMNDEF](./jet-columndef-structure.md) dati.
