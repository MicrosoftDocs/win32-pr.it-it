---
title: Informazioni sull'I/O dei file multimediali
description: Informazioni sull'I/O dei file multimediali
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Multimedia di Windows, I/O file
- Multimedia, I/O file
- input multimediale, I/O file
- I/O file multimediale, informazioni
- I/O di file, informazioni
- input e output (I/O), informazioni
- I/O (input e output), informazioni
- I/O di base
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298261"
---
# <a name="about-multimedia-file-io"></a>Informazioni sull'I/O dei file multimediali

Per la maggior parte delle applicazioni multimediali è necessario l'input e l'output (I/O) del file, ovvero la possibilità di creare, leggere e scrivere file su disco. I servizi di I/O dei file multimediali forniscono I/O di file memorizzati nel buffer e non memorizzati nel buffer e supportano i file RIFF. I servizi sono estendibili con procedure di I/O personalizzate che possono essere condivise tra le applicazioni.

Per la maggior parte delle applicazioni sono necessari solo i servizi di I/O dei file di base e i servizi di I/O file di RIFF. Le applicazioni sensibili alle prestazioni di I/O dei file, ad esempio le applicazioni che trasmettono i dati da Compact Disk in tempo reale, possono ottimizzare le prestazioni usando i servizi per accedere direttamente al buffer di I/O dei file. Le applicazioni che accedono a sistemi di archiviazione personalizzati, ad esempio archivi di file e database, possono fornire una propria procedura di I/O che legge e scrive elementi del sistema di archiviazione.

 

 




