---
title: Effetto morfologia
description: Usare l'effetto morfologia per assottigliare o ispessire i limiti del bordo in un'immagine.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- effetti morfologici
- effetto dilate
- erosione effetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120470"
---
# <a name="morphology-effect"></a>Effetto morfologia

Usare l'effetto morfologia per assottigliare o ispessire i limiti del bordo in un'immagine. Questo effetto crea un kernel che è 2 volte i valori di larghezza e altezza specificati. Questo effetto centra il kernel sul pixel che sta calcolando e restituisce il valore massimo nel kernel (se si dilata) o il valore minimo nel kernel (in caso di erosione).

Il CLSID per questo effetto è CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Immagini di esempio

Questo esempio mostra l'output dell'effetto quando si usa la modalità di erosione.



| Prima                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![immagine dopo la trasformazione.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                          | Tipo e valore predefinito                                                     | Descrizione                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_Modalità prop della morfologia d2d1 \_ \_<br/>     | \_Modalità morfologia d2d1 \_<br/> \_ \_ Erosione della modalità MORFOLOGIa d2d1 \_<br/> | Modalità morfologia. Le modalità disponibili sono Erode (Flat) e dilate (ispessimento).<br/> Per altre informazioni, vedere [modalità di morfologia](#morphology-modes) .<br/> |
| Larghezza<br/> \_Larghezza prop della morfologia d2d1 \_ \_<br/>   | UINT<br/> 1<br/>                                               | Dimensione del kernel nella direzione X. Le unità sono in tuffi. I valori devono essere compresi tra 1 e 100 inclusi.                                                         |
| Altezza<br/> \_Altezza della \_ prop MORFOLOGIa d2d1 \_<br/> | UINT<br/> 1<br/>                                               | Dimensione del kernel nella direzione Y. Le unità sono in tuffi. I valori devono essere compresi tra 1 e 100 inclusi.                                                         |



 

## <a name="morphology-modes"></a>Modalità morfologia



| Nome                           | Descrizione                                                    |
|--------------------------------|----------------------------------------------------------------|
| \_ \_ Erosione della modalità MORFOLOGIa d2d1 \_  | Viene usato il valore massimo di ogni canale RGB nel kernel. |
| \_Modalità morfologia d2d1 \_ \_ dilate | Viene usato il valore minimo di ogni canale RGB nel kernel. |



 

## <a name="output-bitmap"></a>Bitmap di output

Per la modalità dilate, le dimensioni della bitmap di output aumentano: 

| Requisito | Valore |
|--------------------------|-----------------------------------------|
| Aumento dimensioni bitmap di output X = | INT (FLOAT (width) \* ((dpi utente)/96)  |
| Crescita bitmap di output Y = | INT (FLOAT (Height) \* ((dpi utente)/96) |



 

Per la modalità di Erode, le dimensioni della bitmap di output vengono compattate:

| Requisito | Valore |
|--------------------------|------------------------------------------|
| Aumento dimensioni bitmap di output X = | INT (FLOAT (-width) \* ((dpi utente)/96)  |
| Crescita bitmap di output Y = | INT (FLOAT (-Height) \* ((dpi utente)/96)) |



 

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

 

