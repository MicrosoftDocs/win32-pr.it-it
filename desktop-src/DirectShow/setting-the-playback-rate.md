---
description: Impostazione della velocità di riproduzione
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Impostazione della velocità di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303692"
---
# <a name="setting-the-playback-rate"></a>Impostazione della velocità di riproduzione

Per modificare la velocità di riproduzione, chiamare il metodo [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) . Specificare la nuova velocità come frazione della frequenza originale. Per riprodurre, ad esempio, una velocità di due volte normale, utilizzare quanto segue:


```C++
pSeek->SetRate(2.0)
```



Le tariffe maggiori di uno sono più veloci del normale. Le tariffe comprese tra zero e uno sono inferiori al normale. Le frequenze negative sono definite come riproduzione indietro, ma in pratica la maggior parte dei filtri non le supporta. Attualmente nessuno dei filtri DirectShow standard supporta la riproduzione inversa.

Indipendentemente dalla velocità di riproduzione, la posizione corrente e la posizione di arresto sono sempre espresse in relazione all'origine originale. Se, ad esempio, un file di origine è di 20 secondi alla frequenza di riproduzione normale, se si imposta la posizione corrente su 10 secondi verrà cercata al centro del file. Se la frequenza di riproduzione è 2,0, la posizione di arresto è 20 secondi e si cerca la posizione di 10 secondi, il file verrà riprodotto per 5 secondi di tempo reale: 10 secondi, con una doppia velocità di riproduzione normale. Con la velocità di riproduzione 2,0, la posizione corrente aumenta al doppio della frequenza del clock di riferimento.

 

 



