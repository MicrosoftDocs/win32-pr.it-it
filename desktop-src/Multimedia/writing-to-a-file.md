---
title: Scrittura in un file
description: Scrittura in un file
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Funzione AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf46125d9da8b9e5e0668f504028db8b011c99c780b545f9ea99accc0a9ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891771"
---
# <a name="writing-to-a-file"></a>Scrittura in un file

È possibile scrivere informazioni supplementari in un file aperto con privilegi di scrittura usando la [**funzione AVIFileWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) Questa funzione copia le informazioni da un buffer fornito dall'applicazione e le inserisce in uno o più blocchi nel file. Il blocco "INFO" è un tipo di blocco RIFF comune in cui la funzione archivia informazioni supplementari. Per una descrizione dei file RIFF e dei relativi blocchi di dati, vedere [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




