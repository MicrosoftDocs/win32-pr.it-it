---
title: Effetto trasferimento tabella
description: Utilizzare l'effetto di trasferimento tabella per eseguire il mapping delle intensità di colore di un'immagine utilizzando una funzione di trasferimento creata dall'interpolazione di un elenco di valori forniti.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- effetto trasferimento tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476751"
---
# <a name="table-transfer-effect"></a>Effetto trasferimento tabella

Utilizzare l'effetto di trasferimento tabella per eseguire il mapping delle intensità di colore di un'immagine utilizzando una funzione di trasferimento creata dall'interpolazione di un elenco di valori forniti.

Il CLSID per questo effetto è CLSID \_ D2D1TableTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra l'input e l'output dell'effetto di trasferimento tabella.



| Prima                                                         |
|----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)     |
| After                                                          |
| ![immagine dopo la trasformazione.](images/11-tabletransfer.png) |



 


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



La funzione di trasferimento si basa su un elenco di input V = (V0, V1, V2, V3, V? , V<sub>n</sub>), dove N è il numero di elementi-1.

L'intensità dei pixel di input viene rappresentata come C. L'intensità del pixel di output, C può essere calcolata con l'equazione.

Per un valore C, scegliere un valore k, in modo che: k/N = C < (k + 1)/N

L'output C viene calcolato utilizzando l'equazione seguente: C'= V? + (C-k/N) \* n \* (V??? 1? -V?

Questo effetto funziona su immagini alfa diritte e premoltiplicate. L'effetto restituisce bitmap alfa premoltiplicate.

Di seguito è riportato il grafico della funzione di trasferimento della tabella se la proprietà Table è impostata su `[0.0, 0.25, 1.0]` .

![grafico dell'intensità dei pixel per la funzione di trasferimento della tabella.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Proprietà effetto

> [!Note]  
> I valori di tutti i canali delle proprietà di trasferimento della tabella sono privi di unità e hanno un minimo di 0,0 e un massimo di 1,0.

 



| Nome visualizzato e enumerazione dell'indice                                           | Tipo e valore predefinito                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ TABLETRANSFER \_ - \_ \_ tabella rossa<br/>         | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale rosso.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ Red \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso. Se si imposta questa opzione su FALSE, viene applicata la funzione RedTableTransfer al canale rosso.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> \_ \_ \_ Tabella verde prop d2d1 \_ TABLETRANSFER<br/>     | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ Green \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa opzione su FALSE, viene applicata la funzione GreenTableTransfer al canale verde.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> D2D1 \_ TABLETRANSFER \_ - \_ tabella blu Prop \_<br/>       | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale blu.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ Blue \_ Disable<br/>   | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale blu. Se si imposta questa opzione su FALSE, viene applicata la funzione BlueTableTransfer al canale blu.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> Tabella D2D1 per il \_ trasferimento della tabella \_ \_ \_ \_<br/>   | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ Alpha \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale alfa. Se si imposta questa opzione su FALSE, viene applicata la funzione AlphaTableTransfer al canale alfa.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> D2D1 \_ TABLETRANSFER \_ prop \_ \_ output Clamp<br/>   | BOOL<br/> FALSE<br/>             | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

