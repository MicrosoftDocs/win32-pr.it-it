---
description: Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lettura o scrittura in file con uno schema Scatter-Gather scrittura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914481"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lettura o scrittura in file con uno schema Scatter-Gather scrittura

Uno schema di raccolta a dispersione usa il sistema operativo per recapitare in un'unica operazione più blocchi discreti di dati (ad esempio record di database) da un file a buffer separati e non contigui in memoria. Uno schema di raccolta a dispersione scrive anche i dati da buffer non contigui in un'unica operazione.

Un'applicazione può implementare uno schema di raccolta a dispersione usando le [**funzioni ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) [**e WriteFileGather.**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)

 

 



