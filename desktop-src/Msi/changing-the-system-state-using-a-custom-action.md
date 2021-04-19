---
description: Le azioni personalizzate progettate per modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Modifica dello stato del sistema mediante un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310993"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Modifica dello stato del sistema mediante un'azione personalizzata

Le azioni personalizzate progettate per modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata. Le azioni personalizzate che impostano le proprietà, gli Stati delle funzionalità, gli Stati dei componenti o le directory di destinazione o pianificano le operazioni di sistema inserendo righe nelle tabelle di sequenza possono utilizzare l'esecuzione immediata in modo sicuro. Tuttavia, le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione. Per altre informazioni, vedere [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md).

Non tentare di utilizzare un'azione personalizzata di esecuzione immediata per modificare lo stato del sistema, poiché ogni azione personalizzata che modifica lo stato deve disporre di un'azione di rollback personalizzata corrispondente per annullare la modifica dello stato del sistema in caso di rollback dell'installazione. Tutte le azioni personalizzate di rollback sono anche azioni personalizzate posticipate e devono precedere l'azione che vengono annullate. Per altre informazioni, vedere [rollback delle azioni personalizzate](rollback-custom-actions.md).

 

 



