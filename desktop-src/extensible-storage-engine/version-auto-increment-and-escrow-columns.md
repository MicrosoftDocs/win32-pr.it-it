---
description: 'Altre informazioni su: Colonne Version, Auto-Increment e Escrow'
title: Colonne Versione, Incremento automatico e Deposito
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
# <a name="version-auto-increment-and-escrow-columns"></a>Colonne Versione, Incremento automatico e Deposito


_**Si applica a:** Windows | Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>Colonne Versione, Incremento automatico e Deposito

ESE offre tipi di colonna di versione, incremento automatico e aggiornamento del deposito con capacità speciali. Le opzioni di colonna impostate nel membro **grbit** della [struttura JET_COLUMNDEF](./jet-columndef-structure.md) usata nella chiamata a [JetAddColumn](./jetaddcolumn-function.md) indicano se la colonna è uno dei tipi specializzati indicati qui.

### <a name="version-jet_bitcolumnversion"></a>Versione (JET_bitColumnVersion)

L'opzione version column, applicata solo alle colonne JET_coltypLong, indica che la colonna contiene informazioni sulla versione del record che possono essere usate per determinare se è necessario aggiornare una copia in memoria di un determinato record. Le colonne della versione vengono incrementate automaticamente di ESE quando la colonna viene modificata dall'applicazione tramite [JetUpdate.](./jetupdate-function.md)

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>Incremento automatico (JET_bitColumnAutoincrement)

Le colonne con incremento automatico vengono incrementate automaticamente di ESE quando viene inserito un nuovo record nella tabella. Il valore contenuto nella colonna di incremento automatico è univoco per ogni record della tabella e non è garantito che sia continuo. Questi valori non vengono riciclati, ma possono essere riutilizzati in alcuni casi. Solo le colonne di tipo JET_coltypLong e JET_coltypLongLong possono essere colonne a incremento automatico.

### <a name="escrow-jet_bitcolumnescrowupdate"></a>Deposito (JET_bitColumnEscrowUpdate)

Le colonne del deposito possono essere modificate nella chiamata [a JetEscrowUpdate.](./jetescrowupdate-function.md) Gli aggiornamenti nel deposito sono operazioni delta numeriche che non sono erre da conflitti di scrittura. Ciò significa che un numero qualsiasi di sessioni può aggiornare simultaneamente una colonna del deposito in un record tramite [JetEscrowUpdate](./jetescrowupdate-function.md) senza conflitti. Si noti che qualsiasi altra operazione di aggiornamento può comunque causare un conflitto di scrittura con un'operazione di aggiornamento del deposito. Gli aggiornamenti del deposito possono essere emesse solo a colonne di JET_coltypLong che hanno un valore predefinito. Queste colonne devono anche essere aggiunte a una tabella prima che venga caricata con righe. Infine, le righe contenenti una colonna di aggiornamento del deposito possono essere configurate per supportare un callback di finalizzazione delle righe (JET_bitColumnFinalize) o per essere eliminate automaticamente se il conteggio dei riferimenti raggiunge zero (JET_bitColumnDeleteOnZero). Per altre informazioni, vedere la [JET_COLUMNDEF](./jet-columndef-structure.md) struttura .
