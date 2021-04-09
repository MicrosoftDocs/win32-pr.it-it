---
title: Tipo di bitmap
description: Tipo di bitmap
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- informazioni di riferimento per interfacce, bitmap
- bitmap in interfacce, tipi
- bitmap in interfacce, valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856110"
---
# <a name="bitmap-type"></a>Tipo di bitmap

La tabella seguente illustra i valori validi per il tipo di bitmap. È necessario solo il tipo di sfondo; altre sono facoltative e si riferiscono a diversi usi possibili delle immagini.



| Valore       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sfondo  | Obbligatorio. Immagine su cui vengono sovrapposte tutte le immagini dei pulsanti. Le dimensioni dell'immagine di sfondo di base includono la larghezza e l'altezza complete dello schermo. Si tratta anche del file in cui vengono visualizzate le immagini per gli Stati naturali dei pulsanti e degli TrackBar. (I pulsanti push e disabled non fanno parte di questa immagine).                                                                                                                                                                                                                                                                                           |
| Disabled    | Obbligatorio. Indica che il push del pulsante non avrà alcun effetto. Definisce un'immagine che viene visualizzata quando l'utente non dispone di funzionalità specifiche del lettore. È necessario fornire un valore di coordinate per indicare la posizione dell'angolo superiore sinistro dell'immagine rispetto all'immagine di sfondo.                                                                                                                                                                                                                                                                                                                |
| Spinto      | Obbligatorio. Definisce un'immagine visualizzata quando l'utente effettua il push di un pulsante. Usare push per fornire un feedback visivo all'utente quando tocca un pulsante. È necessario fornire un valore di coordinate per indicare la posizione dell'angolo superiore sinistro dell'immagine rispetto all'immagine di sfondo.                                                                                                                                                                                                                                                                                                                              |
| Region      | Definisce immagini che usano aree colorate per rappresentare l'area di risposta tap per i pulsanti di tipo hit: PushHit, ToggleHit, 2PushHit. Se si usano i pulsanti di tipo hit, è necessario specificare un'immagine di area. Questo file di immagine usa colori specifici della tavolozza di Windows per ogni controllo. I colori sono definiti da numeri che rappresentano il valore di rosso, verde e blu per l'area. Questa immagine non viene mai visualizzata dall'utente. È inoltre necessario fornire un valore di coordinate per indicare la posizione dell'angolo superiore sinistro dell'immagine rispetto all'immagine di sfondo.                                                      |
| SeekThumb   | Definisce un'immagine che si utilizzerà insieme a un TrackBar per indicare la posizione corrente nell'elemento multimediale. Se, ad esempio, la riproduzione di un brano è metà, l'immagine SeekThumb viene visualizzata al centro del TrackBar. Toccando e trascinando l'immagine SeekThumb, l'utente può riavviare l'elemento multimediale in qualsiasi posizione, denominato *ricerca*. L'immagine di TrackBar è definita nell'immagine di sfondo. L'immagine SeekThumb non è inclusa nella sezione bitmap del file di definizione dell'interfaccia, ma viene specificata come parte della definizione TrackBar nella sezione TrackBars. |
| Super       | Definisce l'immagine disabilitata per un TrackBar. Può inoltre contenere immagini alternative per il pulsante di silenziamento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| VolumeThumb | Definisce un'immagine da usare insieme a un oggetto TrackBar per indicare la posizione del volume. Toccando e trascinando l'immagine VolumeThumb, l'utente può modificare il livello del volume. L'immagine di TrackBar è definita nell'immagine di sfondo. L'immagine VolumeThumb non è inclusa nella sezione bitmap del file di definizione dell'interfaccia, ma viene specificata come parte della definizione TrackBar nella sezione TrackBars.                                                                                                                                                                                      |



 

> [!Note]  
> I tipi Region e Super bitmap sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.

 

Si noti che il nome del file e il tipo di file non sono necessariamente uguali. È possibile chiamare il file di cui è stato eseguito il push, ma è ancora indicato in altre posizioni come push. Nella sezione Buttons (pulsanti), ad esempio, è presente un elemento, ad esempio:


```C++
Pushed @ 50,60

```



Si riferisce al tipo del file, non al nome del file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Bitmap**](bitmaps.md)
</dt> </dl>

 

 




