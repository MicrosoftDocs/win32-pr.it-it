---
description: Gli handle opachi vengono usati in TSPI per fare riferimento alle strutture di dati che rappresentano linee, telefoni e aspetto delle chiamate.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Handle opachi e strutture di dati private
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966855"
---
# <a name="opaque-handles-and-private-data-structures"></a>Handle opachi e strutture di dati private

Gli handle opachi vengono usati in TSPI per fare riferimento alle strutture di dati che rappresentano linee, telefoni e aspetto delle chiamate. Questi vengono visualizzati come parametri per la maggior parte delle funzioni e dei callback. Sono disponibili poche funzioni che fanno riferimento al dispositivo usando un identificatore di dispositivo anziché un handle opaco. In tal caso, il riferimento è al dispositivo stesso piuttosto che a una struttura di dati. Le funzioni che funzionano in questo modo sono in genere quelle chiamate in fase di inizializzazione anticipata prima della creazione di strutture di dati e lo scambio di handle opachi.

Il provider di servizi deve decidere come interpretare questi handle. Un provider di servizi utilizza in genere il puntatore alla relativa struttura di dati o all'indice in una matrice di strutture di dati come handle opaco. L'unica restrizione è che il provider di servizi non può usare il valore 0 come [HDRVLINE](hdrvline.md), HDRVCALL o [HDRVPHONE](hdrvphone.md). Il valore 0 o **null** per un handle ha un significato speciale in alcune operazioni.

 

 



