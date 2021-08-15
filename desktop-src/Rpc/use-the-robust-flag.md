---
title: Usare il flag /robust
description: Compilare sempre i file con estensione idl usando l'opzione /robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010889"
---
# <a name="use-the-robust-flag"></a>Usare il flag /robust

Compilare sempre i file con estensione idl usando [**l'opzione /robust.**](/windows/desktop/Midl/-robust) L'uso dell'opzione **/robust** genera informazioni aggiuntive che consentono al motore di rappresentazione dei dati di rete (NDR) di eseguire il controllo degli errori di runtime sugli argomenti correlati in matrici dinamiche, unioni e puntatori a interfaccia out nelle applicazioni COM e RPC. Se il software non riesce a compilare con questo flag, il software è così esposto agli attacchi che nessun impegno in altre aree può proteggerlo.

 

 