---
title: Effetto di trasferimento discreto
description: Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento passaggio creata da un elenco di valori specificati.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- effetto di trasferimento discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c977e6d2b03a3496bfa9be84209a32f57094c8514f6760746f9ec967c2ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431415"
---
# <a name="discrete-transfer-effect"></a>Effetto di trasferimento discreto

Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento passaggio creata da un elenco di valori specificati.

Il CLSID per questo effetto è CLSID \_ D2D1DiscreteTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra l'input e l'output dell'effetto di trasferimento discreto.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)        |
| After                                                             |
| ![l'immagine dopo la trasformazione.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



La funzione di trasferimento è basata sull'elenco di input: V=(V0,V1,V2,V3,V? ,V<sub>N</sub>) dove N è il numero di elementi - 1.

L'intensità in pixel di input è rappresentata come C. L'intensità in pixel di output, C, viene calcolata con l'equazione:

Per un valore C, selezionare un valore k, in modo che:

![formula per il processo.](images/discrete-transfer1.png)

L'output C può essere calcolato usando l'equazione: C' = V?

Questo effetto funziona su immagini alfa rette e premoltiliate. L'effetto restituisce bitmap alfa premoltiliate.

Ecco l'aspetto del grafico della funzione di trasferimento discreta se gli input sono `[0.25, 0.5, 0.75, 1.0]` .

![grafico di intensità pixel per la funzione di trasferimento discreto.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Proprietà degli effetti

> [!Note]  
> I valori di tutti i canali delle proprietà di trasferimento discrete sono senza unità e hanno un minimo di 0,0 e un massimo di 1,0.

 



| Enumerazione del nome visualizzato e dell'indice                                              | Tipo e valore predefinito                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> TABELLA ROSSA DELLA PROPRIETÀ \_ DISCRETETRANSFER D2D1 \_ \_ \_<br/>         | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale Rosso.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Rosso. Se si imposta questa proprietà su FALSE, l'effetto applica la funzione RedDiscreteTransfer al canale Red.                                                                                                                                                                                                                                                                 |
| Tabella verde<br/> TABELLA VERDE PROPRIETÀ \_ DISCRETETRANSFER D2D1 \_ \_ \_<br/>     | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa proprietà su FALSE, l'effetto applica la funzione GreenDiscreteTransfer al canale Verde.                                                                                                                                                                                                                                                           |
| BlueTable<br/> TABELLA BLU DELLA PROPRIETÀ \_ DISCRETETRANSFER D2D1 \_ \_ \_<br/>       | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale Blu.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Blu. Se si imposta questa proprietà su FALSE, l'effetto applica la funzione BlueDiscreteTransfer al canale Blue.                                                                                                                                                                                                                                                              |
| Tabella alfa<br/> TABELLA ALFA DELLA PROPRIETÀ \_ DISCRETETRANSFER D2D1 \_ \_ \_<br/>     | Galleggiante\[\]<br/> {0.0f, 1.0f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale Alfa.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Alfa. Se si imposta questa opzione su FALSE, l'effetto applica la funzione AlphaDiscreteTransfer al canale Alfa.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> D2D1 \_ DISCRETETRANSFER \_ PROP \_ CLAMP \_ OUTPUT<br/>   | BOOL<br/> FALSE<br/>             | Indica se l'effetto stringe i valori di colore tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto stringe i valori prima di premultiplare il valore alfa.<br/> Se si imposta questa opzione su TRUE, l'effetto stringerà i valori. Se si imposta questa proprietà su FALSE, l'effetto non stringerà i valori di colore, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficientemente elevata.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

