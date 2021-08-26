---
description: Valore che definisce le unità per un valore di profondità in un fotogramma video.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca57fa5cf72be266ac58ee504b1d4b7c4f2506646f33295e468d2ed0781ab8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060641"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>Attributo \_ MF MT \_ DEPTH \_ VALUE \_ UNIT

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che definisce le unità per un valore di profondità in un fotogramma video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Il valore unitario è un valore UINT64 in nanometri, nell'intervallo da 1e a 9 metri. Se questo valore non è presente, il valore predefinito dell'unità è 1e-3, che indica che ogni livello di pixel viene misurato in 1 millimetro nello spazio fisico.

Le fotocamere di profondità non sono in grado di descrizione della profondità di tutti i pixel. Quando l'attendibilità di un pixel è bassa, a causa di materiale, occlusione o fuori intervallo e così via, il valore di profondità su tale pixel può non essere valido.

Quando un valore in pixel di profondità è 0, il pixel non è valido.

Alcune fotocamere di profondità collegano i metadati della maschera di bit per ogni pixel oltre al valore di profondità per rappresentare il motivo per cui la profondità del pixel non è valida, a causa di materiale, occlusione o fuori intervallo e così via. È consigliabile evitare di associare metadati come valori di bit in profondità, perché in genere causano difficoltà quando si usano tali valori in pixel shader. Invece. È consigliabile usare un buffer immagine separato a 8 bit con la stessa risoluzione e collegarlo come attributo di [**IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Questi metadati variano per ogni fornitore di fotocamere e non sono standardizzati dalla piattaforma. È consigliabile usare 16 bit completi per il valore di profondità per semplificare l'elaborazione downstream e usare un valore fisso, ad esempio 0 per l'invalidamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




