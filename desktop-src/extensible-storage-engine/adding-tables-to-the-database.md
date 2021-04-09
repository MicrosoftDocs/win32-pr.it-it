---
description: 'Altre informazioni su: aggiunta di tabelle al database'
title: Aggiunta di tabelle al database
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966417"
---
# <a name="adding-tables-to-the-database"></a>Aggiunta di tabelle al database


_**Si applica a:** Windows | Windows Server_

## <a name="adding-tables-to-the-database"></a>Aggiunta di tabelle al database

Le tabelle sono una raccolta eterogenea di record che raggruppano fisicamente e logicamente i dati nel database. Le tabelle vengono identificate in modo univoco in base al nome. L'ID tabella ([JET_TABLEID](./jet-tableid.md)) è un handle per un cursore utilizzato per aggiornare e spostarsi tra le tabelle. È possibile aprire più [JET_TABLEID](./jet-tableid.md) nella stessa tabella.

Una tabella esistente viene aperta nella chiamata a [JetOpenTable](./jetopentable-function.md)e viene creata una nuova tabella senza righe o colonne con [JetCreateTable](./jetcreatetable-function.md). Per creare una tabella in modo atomico con un set iniziale di colonne e indici, chiamare [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Le dimensioni iniziali della tabella sono fornite nel parametro *lPages* in [JetCreateTable](./jetcreatetable-function.md) o nel membro **ulPages** della struttura [JET_TABLECREATE](./jet-tablecreate-structure.md) della chiamata a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Le tabelle aumentano automaticamente quando i dati vengono aggiunti alla tabella. La crescita è proporzionale alle dimensioni iniziali della tabella. Le colonne possono essere aggiunte alla tabella in qualsiasi momento con [JetAddColumn](./jetaddcolumn-function.md). Quando l'applicazione non deve più accedere alla tabella, è possibile chiudere il cursore con [JetCloseTable](./jetclosetable-function.md). La tabella può essere eliminata tramite una chiamata a [JetDeleteTable](./jetdeletetable-function.md).

Le operazioni di tabella devono essere eseguite nel contesto di una transazione.

## <a name="see-also"></a>Vedere anche

[Transazioni](./transactions.md)
