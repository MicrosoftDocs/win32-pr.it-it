---
description: Specifica il grado in base al quale il codec deve ridurre l'intervallo di colori effettivo del video.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3a186522cdc328ab7b6f8e11154ae605673d2cca9d988e0e07c0d159e71589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113311"
---
# <a name="mfpkey_rangeredux-property"></a>Proprietà MFPKEY \_ RANGEREDUX

Specifica il grado in base al quale il codec deve ridurre l'intervallo di colori effettivo del video.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Riduzione dell'intervallo specifica il grado di riduzione dell'intervallo luma e chroma del video da parte del codec. La riduzione dell'intervallo riduce le dimensioni dei fotogrammi video codificati, ma riduce anche il dettaglio del colore del video.

La riduzione dell'intervallo è costituita dalla riduzione durante la codifica e l'espansione durante la decodifica. È possibile rendere i fattori di espansione diversi da quelli di riduzione, ma questa operazione non è consigliata nella maggior parte degli scenari in cui il nuovo mapping degli intervalli è utile.

La riduzione e l'espansione dell'intervallo vengono eseguite separatamente sui canali luma e chroma. La riduzione dell'intervallo può essere un modo efficiente per ridurre la complessità dei video a bassa velocità in bit senza compromettere i dettagli dell'immagine. L'impostazione di tutti e quattro i valori su 8 riduce la quantità di informazioni luma e chroma dimesse, lasciando più bit da dirigere al mantenimento dei dettagli dell'immagine.

Il codec può scegliere di usare automaticamente la riduzione dell'intervallo durante la codifica video a velocità in bit molto basse. L'impostazione di tutti e quattro i valori su 0 disabilita completamente la riduzione dell'intervallo anche in scenari con velocità in bit bassa.

La riduzione dell'intervallo di colori riduce le dimensioni codificate dei fotogrammi video, ma può introdurre sfocatezza nei fotogrammi decodificati.

Se questa proprietà non è impostata, il codec determina se usare la riduzione dell'intervallo in fase di codifica. Questa opzione viene in genere selezionata dal codec solo a velocità in bit basse.

Il valore di questa proprietà è una combinazione di quattro componenti, separati da zeri, formattati come 0x0M0m0N0n, dove:

-   M è il fattore di riduzione dell'intervallo di codifica per il componente Y.
-   m è il fattore di espansione dell'intervallo di decodifica per il componente Y (in genere uguale a M).
-   N è il fattore di riduzione dell'intervallo di codifica per il componente UV.
-   n è il fattore di espansione dell'intervallo di decodifica per il componente UV (in genere uguale a N).

Ogni fattore è una cifra da 0 a 8, dove 0 non è una riduzione o un'espansione e 8 è la riduzione o espansione massima.

Se si imposta il valore su 0x00000000, la riduzione dell'intervallo è completamente disabilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




