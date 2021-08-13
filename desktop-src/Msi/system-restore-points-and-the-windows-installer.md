---
description: Ripristino configurazione di sistema monitora e registra automaticamente le modifiche principali del sistema nel computer di un utente. Per altre informazioni, vedere Ripristino configurazione di sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Ripristino configurazione di sistema Points e il programma di Windows di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b8de832208f2bee301a1a159da058ba0f97cf2ecbd74892cb809e1186fbb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624095"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Ripristino configurazione di sistema Points e il programma di Windows di installazione

Ripristino configurazione di sistema monitora e registra automaticamente le modifiche principali del sistema nel computer di un utente. Per altre informazioni, [vedere](../sr/system-restore-portal.md)Ripristino configurazione di sistema .

I punti di ripristino di sistema vengono creati dal sistema e vengono creati anche dal Windows di installazione quando il software viene installato o rimosso.

In Windows XP, il programma di installazione può creare checkpoint durante la prima installazione di un'applicazione e durante la rimozione. Il programma di installazione crea checkpoint solo in questi casi quando la modifica viene eseguita con almeno [*un'interfaccia utente di base.*](b-gly.md) Le installazioni con il [livello di interfaccia](user-interface-levels.md) utente impostato su Nessuno vengono in genere avviate dal sistema o da un'applicazione che deve gestire la creazione di un checkpoint. Per altre informazioni, [vedere](../sr/system-restore-portal.md)Ripristino configurazione di sistema .

Nelle aziende con molte applicazioni di piccole dimensioni, gli amministratori possono decidere di disabilitare il checkpoint dall'interno del programma di installazione per migliorare le prestazioni. Per altre informazioni, vedere [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o [Impostazione di un punto di ripristino da un'azione personalizzata.](setting-a-restore-point-from-a-custom-action.md)

A partire da Windows Installer 5.0, è possibile impostare la proprietà [**MSIFASTINSTALL**](msifastinstall.md) per impedire a un'installazione di generare un punto di ripristino di sistema.

 

 
