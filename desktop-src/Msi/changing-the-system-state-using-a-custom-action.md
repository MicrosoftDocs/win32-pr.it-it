---
description: Le azioni personalizzate destinate a modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Modifica dello stato del sistema tramite un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3ec2fafdc6f57041c087903da0c912327c967b3b188127ee1f2ff71db7c1af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086241"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Modifica dello stato del sistema tramite un'azione personalizzata

Le azioni personalizzate destinate a modificare lo stato del sistema devono essere azioni personalizzate di esecuzione posticipata. Le azioni personalizzate che impostano proprietà, stati delle funzionalità, stati dei componenti o directory di destinazione o pianificano operazioni di sistema inserendo righe nelle tabelle di sequenza possono usare l'esecuzione immediata in modo sicuro. Tuttavia, le azioni personalizzate che modificano direttamente il sistema o chiamano un altro servizio di sistema devono essere rinviate al momento in cui viene eseguito lo script di installazione. Per altre informazioni, vedere [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).

Non è consigliabile provare a usare un'azione personalizzata di esecuzione immediata per modificare lo stato del sistema, perché ogni azione personalizzata che modifica lo stato deve avere un'azione personalizzata di rollback corrispondente per annullare la modifica dello stato del sistema in un rollback dell'installazione. Tutte le azioni personalizzate di rollback sono anche azioni personalizzate posticipate e devono precedere l'azione annullata. Per altre informazioni, vedere [Rollback Custom Actions](rollback-custom-actions.md).

 

 



