---
title: Effetto di trasferimento tabelle
description: Usare l'effetto di trasferimento tabella per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento creata dall'interpolazione di un elenco di valori specificati.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- Effetto di trasferimento tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665010"
---
# <a name="table-transfer-effect"></a>Effetto di trasferimento tabelle

Usare l'effetto di trasferimento tabella per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento creata dall'interpolazione di un elenco di valori specificati.

Il CLSID per questo effetto è CLSID \_ D2D1TableTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra l'input e l'output dell'effetto di trasferimento della tabella.



| Prima                                                         |
|----------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)     |
| After                                                          |
| ![l'immagine dopo la trasformazione.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



La funzione di trasferimento è basata su un elenco di input V=(V0,V1,V2,V3, V? ,V<sub>N</sub>) dove N è il numero di elementi - 1.

L'intensità dei pixel di input è rappresentata come C. L'intensità in pixel di output, C, può essere calcolata con l'equazione.

Per un valore C, selezionare un valore k, in modo che: k/N = C < (k+1)/N

L'output C viene calcolato usando l'equazione seguente: C' = V? + (C - k/N) \* N \* (V??? 1? - V?)

Questo effetto funziona su immagini alfa rette e premoltilied. L'effetto restituisce bitmap alfa premoltilied.

Ecco l'aspetto del grafico della funzione di trasferimento tabelle se la proprietà table è impostata su `[0.0, 0.25, 1.0]` .

![Grafico dell'intensità dei pixel per la funzione di trasferimento tabella.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Proprietà degli effetti

> [!Note]  
> I valori di tutti i canali delle proprietà di trasferimento tabelle sono senza unità e hanno un minimo di 0,0 e un massimo di 1,0.

 



| Nome visualizzato ed enumerazione dell'indice                                           | Tipo e valore predefinito                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> TABELLA D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ TABLE<br/>         | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale rosso.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso. Se si imposta questa opzione su FALSE, la funzione RedTableTransfer viene applicata al canale Red.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> TABELLA VERDE DELLA PROPRIETÀ \_ TABLETRANSFER D2D1 \_ \_ \_<br/>     | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questa opzione su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa opzione su FALSE, la funzione GreenTableTransfer viene applicata al canale verde.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> TABELLA D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_<br/>       | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale Blu.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale blu. Se si imposta questa opzione su FALSE, la funzione BlueTableTransfer viene applicata al canale Blu.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> TABELLA ALFA DELLE PROPRIETÀ \_ \_ DI TRASFERIMENTO \_ TABELLE \_ \_ D2D1<br/>   | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale Alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Alfa. Se si imposta questa opzione su FALSE, la funzione AlphaTableTransfer viene applicata al canale Alpha.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ CLAMP \_ OUTPUT<br/>   | BOOL<br/> FALSE<br/>             | Indica se l'effetto stringe i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto stringe i valori prima che premultipli il valore alfa .<br/> Se si imposta questa proprietà su TRUE, l'effetto anteterà i valori. Se si imposta questa opzione su FALSE, l'effetto non stringerà i valori dei colori, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficiente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

