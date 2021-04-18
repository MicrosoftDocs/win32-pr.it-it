---
title: Scrittura in un file
description: Scrittura in un file
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298525"
---
# <a name="writing-to-a-file"></a>Scrittura in un file

È possibile scrivere informazioni aggiuntive in un file che è stato aperto con privilegi di scrittura tramite la funzione [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) . Questa funzione copia le informazioni da un buffer fornito dall'applicazione e le inserisce in uno o più blocchi del file. Il blocco "INFO" è un tipo di blocco RIFF comune in cui la funzione archivia informazioni supplementari. Per una descrizione dei file RIFF e dei relativi blocchi di dati, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




