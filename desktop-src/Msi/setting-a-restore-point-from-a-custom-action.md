---
description: Le azioni personalizzate non devono chiamare la funzione SRSetRestorePoint perché questo può comportare la scrittura di un punto di ingresso di ripristino nel mezzo di un'installazione di Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Impostazione di un punto di ripristino da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131942"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Impostazione di un punto di ripristino da un'azione personalizzata

Le azioni personalizzate non devono chiamare la funzione [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) perché questo può comportare la scrittura di un punto di ingresso di ripristino nel mezzo di un'installazione di Windows Installer.

Per ulteriori informazioni, vedere [punti di ripristino del sistema e il Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
