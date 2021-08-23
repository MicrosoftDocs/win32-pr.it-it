---
description: Le azioni personalizzate non devono chiamare la funzione SRSetRestorePoint perché ciò potrebbe comportare la scrittura di un punto di ingresso di ripristino al centro di un Windows installazione del programma di installazione.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Impostazione di un punto di ripristino da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628581"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Impostazione di un punto di ripristino da un'azione personalizzata

Le azioni personalizzate non devono chiamare la [**funzione SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) perché ciò potrebbe comportare la scrittura di un punto di ingresso di ripristino al centro di un'installazione Windows installer.

Per altre informazioni, vedere [Ripristino configurazione di sistema Points e il programma di installazione Windows.](system-restore-points-and-the-windows-installer.md)

 

 
