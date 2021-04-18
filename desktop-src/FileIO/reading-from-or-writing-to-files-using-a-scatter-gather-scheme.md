---
description: Descrive uno schema di raccolta a dispersione per la lettura o la scrittura di blocchi di dati non contigui in un'unica operazione.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315929"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lettura o scrittura nei file utilizzando uno schema di Scatter-Gather

Uno schema di raccolta a dispersione usa il sistema operativo per recapitare in una sola operazione più blocchi discreti di dati, ad esempio i record del database, da un file a buffer separati non contigui in memoria. Uno schema a dispersione-raccolta scrive anche i dati da buffer non contigui in un'unica operazione.

Un'applicazione può implementare uno schema di raccolta a dispersione usando le funzioni [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .

 

 



