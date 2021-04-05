---
title: Flag di priorità
description: Il flag Priority apre un oggetto di archiviazione in modalità Priority.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Flag di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045397"
---
# <a name="priority-flags"></a>Flag di priorità

Il flag Priority apre un oggetto di archiviazione in modalità Priority. Quando viene aperto un oggetto, un'applicazione funziona in genere da una copia snapshot, perché anche altre applicazioni possono utilizzare l'oggetto contemporaneamente. Quando si apre un oggetto di archiviazione in modalità di priorità, l'applicazione dispone tuttavia dei diritti esclusivi per eseguire il commit delle modifiche apportate all'oggetto.

La modalità di priorità consente a un'applicazione di leggere alcuni flussi dallo spazio di archiviazione prima di aprire l'oggetto in una modalità che richiederebbe al sistema di creare una copia snapshot. Poiché l'applicazione dispone di accesso esclusivo, non è necessario creare una copia snapshot dell'oggetto. Quando l'applicazione apre successivamente l'oggetto in una modalità in cui è necessaria una copia snapshot, l'applicazione può escludere i flussi che ha già letto dallo snapshot, riducendo così il sovraccarico di apertura dell'oggetto.

Poiché altre applicazioni non possono eseguire il commit delle modifiche in un oggetto mentre è aperto in modalità di priorità, le applicazioni devono tenere l'oggetto in tale modalità per il minor tempo possibile.

 

 




