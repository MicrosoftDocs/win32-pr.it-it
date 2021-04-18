---
description: Un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni LZSeek e LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lettura da file compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315930"
---
# <a name="reading-from-compressed-files"></a>Lettura da file compressi

Oltre a decomprimere un file completo in un'unica operazione, un'applicazione può decomprimere un file compresso una parte alla volta usando le funzioni [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) e [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) . Queste funzioni sono particolarmente utili quando è necessario estrarre parti di file di grandi dimensioni. Un produttore di tipi di carattere, ad esempio, può disporre di file compressi contenenti metriche di tipo carattere oltre ai dati di tipo carattere. Per usare le informazioni contenute in questi file, un'applicazione deve decomprimere il file. Tuttavia, la maggior parte delle applicazioni utilizzerà solo una parte del file in un determinato momento. Per ottenere informazioni sulle metriche dei tipi di carattere, l'applicazione estrae i dati dall'intestazione. Per ottenere informazioni dal testo, l'applicazione riposiziona il puntatore del file chiamando **LZSeek** ed estrae i dati di tipo carattere chiamando **LZRead**.

 

 



