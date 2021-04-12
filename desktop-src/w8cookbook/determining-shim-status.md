---
title: Determinazione dello stato dello shim
description: Determinazione dello stato dello shim
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331727"
---
# <a name="determining-shim-status"></a>Determinazione dello stato dello shim

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8  
Server-Windows Server 2012  
</dl>

## <a name="description"></a>Descrizione

Windows 8 registra gli eventi quando le app vengono sottoposto a shim per vari motivi. Il modo più semplice per determinare se l'app è sottoposto a shim consiste nel controllare il Visualizzatore eventi. Passare a registri applicazioni e servizi \\ Microsoft Windows Application-Experience \\ telemetria del programma.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Il modo migliore per uscire da spessoramento consiste nel rinominare il file eseguibile o aumentare la versione principale di 1 (ricompilare il file eseguibile).

 

 




