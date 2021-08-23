---
title: Informazioni sull'I/O di file multimediali
description: Informazioni sull'I/O di file multimediali
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimediali, I/O di file
- multimediali,I/O di file
- input multimediale, I/O di file
- I/O di file multimediali, informazioni su
- I/O di file, informazioni su
- input e output (I/O), informazioni
- I/O (input e output), informazioni
- I/O di base
- resource interchange file format (RIFF)
- RIFF (formato di file di interscambio di risorse)
- RIFF I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584b736ba41fb0ea7dd5f3e6411e1783964db21a9819fbb98364708196dc2943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526641"
---
# <a name="about-multimedia-file-io"></a>Informazioni sull'I/O di file multimediali

La maggior parte delle applicazioni multimediali richiede l'input e l'output (I/O) dei file, ovvero la possibilità di creare, leggere e scrivere file su disco. I servizi di I/O di file multimediali forniscono I/O di file memorizzati nel buffer e senza buffer e il supporto per i file RIFF. I servizi sono estendibili con procedure di I/O personalizzate che possono essere condivise tra le applicazioni.

Per la maggior parte delle applicazioni sono necessari solo i servizi di I/O di file di base e i servizi di I/O di file RIFF. Le applicazioni sensibili alle prestazioni di I/O dei file, ad esempio le applicazioni che ese streaming di dati da compact disc in tempo reale, possono ottimizzare le prestazioni usando i servizi per accedere direttamente al buffer di I/O di file. Le applicazioni che accedono a sistemi di archiviazione personalizzati, ad esempio archivi di file e database, possono fornire la propria procedura di I/O che legge e scrive elementi del sistema di archiviazione.

 

 




