---
description: Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente. Per ulteriori informazioni, vedere Ripristino configurazione di sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Punti di ripristino del sistema e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308671"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Punti di ripristino del sistema e Windows Installer

Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente. Per ulteriori informazioni, vedere [Ripristino configurazione di sistema](../sr/system-restore-portal.md).

I punti di ripristino del sistema vengono creati dal sistema e vengono creati anche da Windows Installer quando il software viene installato o rimosso.

In Windows XP il programma di installazione può creare checkpoint durante la prima installazione di un'applicazione e durante la relativa rimozione. In questi casi, il programma di installazione crea solo checkpoint quando la modifica viene eseguita con almeno un' [*interfaccia utente di base*](b-gly.md). Le installazioni con il [livello di interfaccia utente](user-interface-levels.md) impostato su None vengono in genere avviate dal sistema o da un'applicazione che deve gestire la creazione di un checkpoint. Per ulteriori informazioni, vedere [Ripristino configurazione di sistema](../sr/system-restore-portal.md).

Nelle aziende con molte piccole applicazioni, gli amministratori possono decidere di disabilitare il checkpoint dall'interno del programma di installazione per migliorare le prestazioni. Per altre informazioni, vedere [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o [impostazione di un punto di ripristino da un'azione personalizzata](setting-a-restore-point-from-a-custom-action.md).

A partire da Windows Installer 5,0, la proprietà [**MSIFASTINSTALL**](msifastinstall.md) può essere impostata in modo da impedire che un'installazione generi un punto di ripristino del sistema.

 

 
