---
title: Effetto trasferimento discreto
description: Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento dei passaggi creata da un elenco di valori forniti.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- effetto trasferimento discreto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104570432"
---
# <a name="discrete-transfer-effect"></a>Effetto trasferimento discreto

Usare l'effetto di trasferimento discreto per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione di trasferimento dei passaggi creata da un elenco di valori forniti.

Il CLSID per questo effetto è CLSID \_ D2D1DiscreteTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'immagine mostra l'input e l'output dell'effetto di trasferimento discreto.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)        |
| After                                                             |
| ![immagine dopo la trasformazione.](images/12-discretetransfer.png) |



 


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



La funzione Transfer è basata sull'elenco di input: V = (V0, V1, V2, V3, V? , V<sub>n</sub>), dove N è il numero di elementi-1.

L'intensità dei pixel di input viene rappresentata come C. L'intensità del pixel di output, C viene calcolata con l'equazione:

Per un valore C, scegliere un valore k, in modo che:

![formula per il processo.](images/discrete-transfer1.png)

L'output C può essere calcolato usando l'equazione: C'= V?

Questo effetto funziona su immagini alfa diritte e premoltiplicate. L'effetto restituisce bitmap alfa premoltiplicate.

Di seguito è riportato il grafico della funzione di trasferimento discreto come se gli input fossero `[0.25, 0.5, 0.75, 1.0]` .

![grafico dell'intensità dei pixel per la funzione di trasferimento discreto.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Proprietà effetto

> [!Note]  
> I valori di tutti i canali delle proprietà di trasferimento discreto sono privi di unità e hanno un minimo di 0,0 e un massimo di 1,0.

 



| Nome visualizzato e enumerazione dell'indice                                              | Tipo e valore predefinito                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ DISCRETETRANSFER \_ - \_ \_ tabella rossa<br/>         | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori utilizzati per definire la funzione di trasferimento per il canale rosso.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ Red \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso. Se si imposta questa opzione su FALSE, l'effetto applica la funzione RedDiscreteTransfer al canale rosso.                                                                                                                                                                                                                                                                 |
| GreenTable<br/> \_ \_ \_ Tabella verde prop d2d1 \_ DISCRETETRANSFER<br/>     | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ Green \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa opzione su FALSE, l'effetto applica la funzione GreenDiscreteTransfer al canale verde.                                                                                                                                                                                                                                                           |
| BlueTable<br/> D2D1 \_ DISCRETETRANSFER \_ - \_ tabella blu Prop \_<br/>       | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale blu.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ Blue \_ Disable<br/>   | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale blu. Se si imposta questa opzione su FALSE, l'effetto applica la funzione BlueDiscreteTransfer al canale blu.                                                                                                                                                                                                                                                              |
| AlphaTable<br/> \_Tabella d2d1 DISCRETETRANSFER \_ prop \_ Alpha \_<br/>     | FLOAT\[\]<br/> {0,0 f, 1.0 f}<br/> | Elenco di valori che definiscono la funzione di trasferimento per il canale alfa.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ Alpha \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale alfa. Se si imposta questa opzione su FALSE, l'effetto applica la funzione AlphaDiscreteTransfer al canale alfa.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ \_ output Clamp<br/>   | BOOL<br/> FALSE<br/>             | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> |



 

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

 

