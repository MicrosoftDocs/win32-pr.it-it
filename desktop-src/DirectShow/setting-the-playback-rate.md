---
description: Impostazione della velocità di riproduzione
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Impostazione della velocità di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0404e67d716616a4c383c134a4fb4e75060e3094023abec52df1d38099b92b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583321"
---
# <a name="setting-the-playback-rate"></a>Impostazione della velocità di riproduzione

Per modificare la velocità di riproduzione, chiamare il [**metodo IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) Specificare la nuova tariffa come frazione della tariffa originale. Ad esempio, per riprodurre a velocità doppia normale, usare quanto segue:


```C++
pSeek->SetRate(2.0)
```



Le tariffe maggiori di una sono più veloci del normale. Le tariffe tra zero e uno sono più lente del normale. Le percentuali negative sono definite come riproduzione all'indietro, ma in pratica la maggior parte dei filtri non la supporta. Attualmente nessuno dei filtri standard DirectShow supporta la riproduzione inversa.

Indipendentemente dalla velocità di riproduzione, la posizione corrente e la posizione di arresto vengono sempre espresse rispetto all'origine originale. Ad esempio, se un file di origine ha una durata di 20 secondi alla velocità di riproduzione normale, impostando la posizione corrente su 10 secondi verrà cercato al centro del file. Se la velocità di riproduzione è 2,0, la posizione di arresto è di 20 secondi e si cerca la posizione di 10 secondi, il file verrà riprodotto per 5 secondi di tempo reale: 10 secondi, al doppio della velocità di riproduzione normale. Con una velocità di riproduzione di 2,0, la posizione corrente aumenta al doppio della velocità dell'orologio di riferimento.

 

 



